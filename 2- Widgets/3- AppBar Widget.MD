### AppBar Widget

AppBar is usually the topmost component of the app (or sometimes the bottom-most),
it contains the toolbar and some other common action buttons.

Key Properties of Appbar Widget:
actions: This property takes in a list of widgets as a parameter to be 
displayed after the title if the AppBar is a row.
title: This property usually takes in the main widget as a parameter 
to be displayed in the AppBar.
backgroundColor: This property is used to add colors to the background of the Appbar.
elevation: This property is used to set the z-coordinate at which to place 
this app bar relative to its parent.
shape: This property is used to give shape to the Appbar and manage its shadow.

Example 1:-

```
import 'package:flutter/material.dart';

void main() {
runApp(gfgApp()); //MaterialApp
}

MaterialApp gfgApp() {
return MaterialApp(
	home: Scaffold(
	appBar: AppBar(
		title: const Text('GeeksforGeeks'),
	), //AppBar
	body: const Center(
		child: Text(
		'GeeksforGeeks',
		style: TextStyle(fontSize: 24),
		), //Text
	), // center
	), //Scaffold
	debugShowCheckedModeBanner: false, //Removing Debug Banner
);
}

```
Example 2:-
```
import "package:flutter/material.dart";

// function to trigger the build process
void main() {
runApp(MyApp()); //MaterialApp
}

// ignore: non_constant_identifier_names
MaterialApp MyApp() {
return MaterialApp(
	home: Scaffold(
	appBar: AppBar(
		title: const Text("GeeksforGeeks"),
		titleSpacing: 00.0,
		centerTitle: true,
		toolbarHeight: 60.2,
		toolbarOpacity: 0.8,
		shape: const RoundedRectangleBorder(
		borderRadius: BorderRadius.only(
			bottomRight: Radius.circular(25),
			bottomLeft: Radius.circular(25)),
		),
		elevation: 0.00,
		backgroundColor: Colors.greenAccent[400],
	), //AppBar
	body: const Center(
		child: Text(
		'GeeksforGeeks',
		style: TextStyle(fontSize: 24),
		),
	), //Center
	), //Scaffold
	debugShowCheckedModeBanner: false, //Removing Debug Banner
);
}

```

Example 3:-

```
import "package:flutter/material.dart";
import 'package:flutter/services.dart';

void main() {
runApp(gfgApp()); //MaterialApp
}

MaterialApp gfgApp() {
return MaterialApp(
	home: Scaffold(
	appBar: AppBar(
		title: const Text("GeeksforGeeks"),
		actions: <Widget>[
		IconButton(
			icon: const Icon(Icons.comment),
			tooltip: 'Comment Icon',
			onPressed: () {},
		), //IconButton
		IconButton(
			icon: const Icon(Icons.settings),
			tooltip: 'Setting Icon',
			onPressed: () {},
		), //IconButton
		], //<Widget>[]
		backgroundColor: Colors.greenAccent[400],
		elevation: 50.0,
		leading: IconButton(
		icon: const Icon(Icons.menu),
		tooltip: 'Menu Icon',
		onPressed: () {},
		),
		systemOverlayStyle: SystemUiOverlayStyle.light,
	), //AppBar
	body: const Center(
		child: Text(
		"Geeksforgeeks",
		style: TextStyle(fontSize: 24),
		), //Text
	), //Center
	), //Scaffold
	debugShowCheckedModeBanner: false, //Removing Debug Banner
);
}

```