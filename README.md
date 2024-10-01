# counter_app_with_provider

## State Management in Flutter with Provider!

Hello there, fellow Flutter adventurers! 👋

This repository contains the source code for the tutorial **[State Management in Flutter with Provider!](https://medium.com/@tech.ramakanttiwari/state-management-in-flutter-with-provider-89fc16ae7700)** published on Medium. This code demonstrates how to manage state effectively in Flutter apps using the Provider package, making complex state management a breeze.

## Table of Contents
- [Overview](#Overview)
- [Features](#Features)
- [Installation](#Installation)
- [Usage](#Usage)
- [Contributing](#Contributing)
- [License](#License)
- [Contact](#Contact)

## Overview
Managing state in a growing Flutter app can get out of hand if you're only using `setState()`. In this project, we explore how to use **Provider** to better manage state, making your app more scalable and maintainable.

This is the accompanying code for my [article](https://medium.com/@tech.ramakanttiwari/state-management-in-flutter-with-provider-89fc16ae7700) that walks you through setting up Provider step by step, from beginner-friendly basics to advanced state management techniques.

## Features
- **Provider Package**: The project implements Flutter's official state management solution.
- **Easy to follow**: Code is structured for easy understanding, with comments and documentation.
- **Scalable**: Example showcases how state management can scale for larger applications.

## Installation
1. Clone the repository:

    ```bash
    git clone https://github.com/tech-ramakant/counter-app-with-provider.git
    ```

2. Navigate to the project directory:

    ```bash
    cd counter-app-with-provider
    ```

3. Install the dependencies:

    ```bash
    flutter pub get
    ```

4. Run the app:

    ```bash
    flutter run
    ```

## Usage

Explore the code in the `lib/` folder to see how the **Provider** package is used to manage state efficiently. You can follow along with the steps in the [Medium tutorial](https://medium.com/@tech.ramakanttiwari/state-management-in-flutter-with-provider-89fc16ae7700).

Example of a state management pattern:

```dart
class CounterModel extends ChangeNotifier {
  int _counter = 0;

  int get counter => _counter;

  void increment() {
    _counter++;
    notifyListeners();
  }
}

class CounterScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return ChangeNotifierProvider(
      create: (_) => CounterModel(),
      child: Scaffold(
        appBar: AppBar(title: Text('Counter App')),
        body: Center(
          child: Consumer<CounterModel>(
            builder: (context, model, child) => Text('Counter: ${model.counter}'),
          ),
        ),
        floatingActionButton: FloatingActionButton(
          onPressed: () => context.read<CounterModel>().increment(),
          child: Icon(Icons.add),
        ),
      ),
    );
  }
}

```

## Contributing
Feel free to open issues or make pull requests to improve this project. Contributions are always welcome!

Fork the repo
- Create your branch: git checkout -b my-new-feature
- Commit your changes: git commit -am 'Add some feature'
- Push to the branch: git push origin my-new-feature
- Submit a pull request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For any inquiries, feel free to reach out to me via:

- Email: [tech.ramakanttiwari@gmail.com](mailto:tech.ramakanttiwari@gmail.com)
- Medium: [@tech.ramakant](https://medium.com/@tech.ramakant)
- LinkedIn: [@tech-ramakant](https://www.linkedin.com/in/ramakant-tiwari-593479128)
- YouTube: [@Tech.Ramakant](https://www.youtube.com/@Tech.Ramakant)

