### Scaffold class in Flutter with Examples
Scaffold is a class in flutter which provides many widgets or we can say APIs 
like Drawer, Snack-Bar, Bottom-Navigation-Bar, Floating-Action-Button, App-Bar, etc.

Properties of Scaffold Class:  
1. app-Bar: It displays a horizontal bar which mainly placed at the top of the Scaffold.

```
Widget build(BuildContext context)
{
return Scaffold(
	appBar: AppBar(
	title: const Text('GeeksforGeeks'),
	),
```

2. body: It will display the main or primary content in the Scaffold.

```
Widget build(BuildContext context) {
return Scaffold(
	appBar: AppBar(title: const Text('GeeksforGeeks')),
	body: const Center(
	child: Text(
		"Welcome to GeeksforGeeks!!!",
		style: TextStyle(
		color: Colors.black,
		fontSize: 40.0,
		),
	),
	),
);
}

```
3. floatingActionButton: FloatingActionButton is a button that is placed at the right bottom corner by default. 

```
Widget build(BuildContext context) {
return Scaffold(
	appBar: AppBar(title: const Text('GeeksforGeeks')),
	body: const Center(
	child: Text(
		"Welcome to GeeksforGeeks!!!",
		style: TextStyle(
		color: Colors.black,
		fontSize: 40.0,
		),
	),
	),
	floatingActionButton: FloatingActionButton(
	elevation: 10.0,
	child: const Icon(Icons.add),
	onPressed: () {
		// action on button press
	},
	),
);
}

```
4. drawer: drawer is a slider menu or a panel which is displayed at the side of the Scaffold.

```
drawer: Drawer(
child: ListView(
	children: const <Widget>[
	DrawerHeader(
		decoration: BoxDecoration(
		color: Colors.green,
		),
		child: Text(
		'GeeksforGeeks',
		style: TextStyle(
			color: Colors.green,
			fontSize: 24,
		),
		),
	),
	ListTile(
		title: Text('Item 1'),
        leading: Icon(Icons.people) 
	),
	ListTile(
		title: Text('Item 2'),
        leading: Icon(Icons.mail) 
	),
	],
),
),
```
5. bottomNavigationBar: bottomNavigationBar is like a menu at the bottom of the Scaffold.

```
bottomNavigationBar: BottomNavigationBar(
		currentIndex: 0,
		fixedColor: Colors.green,
		items: const [
		BottomNavigationBarItem(
			label: "Home",
			icon: Icon(Icons.home),
		),
		BottomNavigationBarItem(
			label: "Search",
			icon: Icon(Icons.search),
		),
		BottomNavigationBarItem(
			label: "Profile",
			icon: Icon(Icons.account_circle),
		),
		],
		onTap: (int indexOfItem) {}),

```
### MaterialApp 
MaterialApp Class: MaterialApp is a predefined class or widget in a flutter. 
It is likely the main or core component of a flutter app.