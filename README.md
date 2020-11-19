# flutter_ticket_widget

A new Flutter package which helps you to implement Ticket Widget in your app.


## 💻 Installation

In the `dependencies:` section of your `pubspec.yaml`, add the following line:

```yaml
flutter_ticket_widget: <latest_version>
```

Import in your project:
```dart
import 'package:flutter_ticket_widget/flutter_ticket_widget.dart';
```

## ❔Basic Usage
```dart
class HomeScreen extends StatefulWidget {
  @override
  _HomeScreenState createState() => _HomeScreenState();
}

class _HomeScreenState extends State<HomeScreen> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.black,
      body: Center(
        child: FlutterTicketWidget(
          width: 350.0,
          height: 500.0,
          isCornerRounded: true,
          child: Padding(
            padding: const EdgeInsets.all(20.0),
            child: Column(
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                Row(
                  mainAxisAlignment: MainAxisAlignment.spaceBetween,
                  children: <Widget>[
                    Container(
                      width: 120.0,
                      height: 25.0,
                      decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(30.0),
                        border: Border.all(width: 1.0, color: Colors.green),
                      ),
                      child: Center(
                        child: Text(
                          'Business Class',
                          style: TextStyle(color: Colors.green),
                        ),
                      ),
                    ),
                    Row(
                      children: <Widget>[
                        Text(
                          'SLM',
                          style: TextStyle(
                              color: Colors.black, fontWeight: FontWeight.bold),
                        ),
                        Padding(
                          padding: const EdgeInsets.only(left: 8.0),
                          child: Icon(
                            Icons.flight_takeoff,
                            color: Colors.pink,
                          ),
                        ),
                        Padding(
                          padding: const EdgeInsets.only(left: 8.0),
                          child: Text(
                            'BTL',
                            style: TextStyle(
                                color: Colors.black,
                                fontWeight: FontWeight.bold),
                          ),
                        )
                      ],
                    )
                  ],
                ),
                Padding(
                  padding: const EdgeInsets.only(top: 20.0),
                  child: Text(
                    'Flight Ticket',
                    style: TextStyle(
                        color: Colors.black,
                        fontSize: 20.0,
                        fontWeight: FontWeight.bold),
                  ),
                ),
                Padding(
                  padding: const EdgeInsets.only(top: 25.0),
                  child: Column(
                    children: <Widget>[
                      ticketDetailsWidget(
                          'Passengers', 'Ilona', 'Date', '24-12-2018'),
                      Padding(
                        padding: const EdgeInsets.only(top: 12.0, right: 40.0),
                        child: ticketDetailsWidget(
                            'Flight', '76836A45', 'Gate', '66B'),
                      ),
                      Padding(
                        padding: const EdgeInsets.only(top: 12.0, right: 40.0),
                        child: ticketDetailsWidget(
                            'Class', 'Business', 'Seat', '21B'),
                      ),
                    ],
                  ),
                ),
                
                Padding(
                  padding: const EdgeInsets.only(top: 80.0, left: 30.0, right: 30.0),
                  child: Container(
                    width: 250.0,
                    height: 60.0,
                    decoration: BoxDecoration(
                        image: DecorationImage(
                            image: AssetImage('assets/barcode.png'),
                            fit: BoxFit.cover)),
                  ),
                ),
                Padding(
                  padding:
                      const EdgeInsets.only(top: 10.0, left: 75.0, right: 75.0),
                  child: Text(
                    '9824 0972 1742 1298',
                    style: TextStyle(
                      color: Colors.black,
                    ),
                  ),
                )
              ],
            ),
          ),
        ),
      ),
    );
  }

  Widget ticketDetailsWidget(String firstTitle, String firstDesc,
      String secondTitle, String secondDesc) {
    return Row(
      mainAxisAlignment: MainAxisAlignment.spaceBetween,
      children: <Widget>[
        Padding(
          padding: const EdgeInsets.only(left: 12.0),
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: <Widget>[
              Text(
                firstTitle,
                style: TextStyle(
                  color: Colors.grey,
                ),
              ),
              Padding(
                padding: const EdgeInsets.only(top: 4.0),
                child: Text(
                  firstDesc,
                  style: TextStyle(
                    color: Colors.black,
                  ),
                ),
              )
            ],
          ),
        ),
        Padding(
          padding: const EdgeInsets.only(right: 20.0),
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: <Widget>[
              Text(
                secondTitle,
                style: TextStyle(
                  color: Colors.grey,
                ),
              ),
              Padding(
                padding: const EdgeInsets.only(top: 4.0),
                child: Text(
                  secondDesc,
                  style: TextStyle(
                    color: Colors.black,
                  ),
                ),
              )
            ],
          ),
        )
      ],
    );
  }
}
```
## Screenshots

| Flutter Ticket Widget                                                                                                          | Example UI                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| ![flutter_ticket_widget](https://user-images.githubusercontent.com/35039342/56443230-57320300-6311-11e9-80c5-d5d79f462dd9.png) | ![example](https://user-images.githubusercontent.com/35039342/56443240-644ef200-6311-11e9-8e2f-26098ebb3d40.png) |


# 👍 How to Contribute

1. Fork it
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create new Pull Request


