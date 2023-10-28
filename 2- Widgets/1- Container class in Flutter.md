### Container class in Flutter

Container class in flutter is a convenience widget that combines common painting, 
positioning, and sizing of widgets. 

Properties of Container Class:

1. child: Container widget has a property ‘child:’ which stores its children. 
The child class can be any widget. 
Let us take an example, taking a text widget as a child. 

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		child:const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}

```
2. color:  The color property sets the background color of the entire container. 

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
		home
		: Scaffold(appBar
				: AppBar(title
							: const Text("Container example"),
						),
					body
				: Container(color
							: Colors.purple,
							child
							: const Text("Hello! i am inside a container!",
									style
									: TextStyle(fontSize : 20)),
							),
				), 
	);
}
}
```
3. height and width: By default, a container class takes the space 
that is required by the child.

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		height: 200,
		width: double.infinity,
		color: Colors.purple,
		child: const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}

```

4. margin: The margin is used to create an empty space around the container.
```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		height: 200,
		width: double.infinity,
		color: Colors.purple,
		margin: const EdgeInsets.all(20),
		child: const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}

```
5. padding: The padding is used to give space from the border 
of the container from its children.

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		height: 200,
		width: double.infinity,
		color: Colors.purple,
		margin: const EdgeInsets.all(20),
		padding: const EdgeInsets.all(30),
		child: const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}

```

6. alignment: The alignment is used to position the child within the container.

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		height: 200,
		width: double.infinity,
		color: Colors.purple,
		alignment: Alignment.bottomCenter,
		margin: const EdgeInsets.all(20),
		padding: const EdgeInsets.all(30),
		child: const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}

```
7. Decoration: The decoration property is used to decorate the box(e.g. give a border).

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		height: 200,
		width: double.infinity,
		//color: Colors.purple,
		alignment: Alignment.center,
		margin: const EdgeInsets.all(20),
		padding: const EdgeInsets.all(30),
		decoration: BoxDecoration(
			border: Border.all(color: Colors.black, width: 3),
		),
		child: const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}

```

8. Transform: This property of the container helps us to rotate the container.

```
import 'package:flutter/material.dart';

void main() => runApp(const MyApp());

class MyApp extends StatelessWidget {
const MyApp({Key? key}) : super(key: key);

@override
Widget build(BuildContext context) {
	return MaterialApp(
	home: Scaffold(
		appBar: AppBar(
		title: const Text("Container example"),
		),
		body: Container(
		height: 200,
		width: double.infinity,
		color: Colors.purple,
		alignment: Alignment.center,
		margin: const EdgeInsets.all(20),
		padding: const EdgeInsets.all(30),
		transform: Matrix4.rotationZ(0.1),
		child: const Text("Hello! i am inside a container!",
			style: TextStyle(fontSize: 20)),
		),
	),
	);
}
}
```