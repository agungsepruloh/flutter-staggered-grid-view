# flutter_staggered_grid_view

A Flutter staggered grid view which supports multiple columns with rows of varying sizes.
![Screenshot](https://raw.githubusercontent.com/letsar/flutter_staggered_grid_view/master/doc/images/example_01.PNG)

## Features

* Configurable cross-axis count or max cross-axis extent like the [GridView](https://docs.flutter.io/flutter/widgets/GridView-class.html)
* Tiles can have a fixed main-axis extent, or a multiple of the cell's length.
* Configurable main-axis and cross-axis margins between tiles.
* SliverStaggeredGrid for using in a [CustomScrollView](https://docs.flutter.io/flutter/widgets/CustomScrollView-class.html).
* Staggered and Spannable grid layouts.

![Screenshot](https://raw.githubusercontent.com/letsar/flutter_staggered_grid_view/master/doc/images/staggered_1.gif)
![Screenshot](https://raw.githubusercontent.com/letsar/flutter_staggered_grid_view/master/doc/images/spannable_1.gif)

## Getting started

In the `pubspec.yaml` of your flutter project, add the following dependency:

```yaml
dependencies:
  ...
  flutter_staggered_grid_view: "^0.1.0"
```

In your library add the following import:

```dart
import 'package:flutter_staggered_grid_view/flutter_staggered_grid_view.dart';
```

For help getting started with Flutter, view the online [documentation](https://flutter.io/).

## Example

![Screenshot_Example](https://raw.githubusercontent.com/letsar/flutter_staggered_grid_view/master/doc/images/example_02.PNG)

```dart
new StaggeredGridView.countBuilder(
  crossAxisCount: 4,
  itemCount: 8,
  itemBuilder: (BuildContext context, int index) => new Container(
      color: Colors.green,
      child: new Center(
        child: new CircleAvatar(
          backgroundColor: Colors.white,
          child: new Text('$index'),
        ),
      )),
  staggeredTileBuilder: (int index) =>
      new StaggeredTile.count(2, index.isEven ? 2 : 1),
  mainAxisSpacing: 4.0,
  crossAxisSpacing: 4.0,
)
```

You can find more examples in the [Example](https://github.com/letsar/flutter_staggered_grid_view/tree/master/example) project.

## Constructors

The `StaggeredGridView` follow the same constructors convention than the [GridView](https://docs.flutter.io/flutter/widgets/GridView-class.html).  
There are two more constructors: `countBuilder` and `extentBuilder`. These constructors allow you to define a builder for the layout and a builder for the children.

## Changelog

Please see the [Changelog](https://github.com/letsar/flutter_staggered_grid_view/blob/master/CHANGELOG.md) page to know what's recently changed.

## Contributions

Feel free to contribute to this project.

If you find a bug or want a feature, but don't know how to fix/implement it, please fill an [issue](https://github.com/letsar/flutter_staggered_grid_view/issues).  
If you fixed a bug or implemented a new feature, please send a [pull request](https://github.com/letsar/flutter_staggered_grid_view/pulls).
