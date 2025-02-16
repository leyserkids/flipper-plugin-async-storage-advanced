# Flipper Async Storage Advanced plugin

## Introduction

This plugin is designed to work with Flipper (https://fbflipper.com/) and Async Storage (https://github.com/react-native-async-storage/async-storage) library.

The plugin provides standard read/write/delete/update operations on the Async Storage keys in React Native applications.

![plugin_video](images/output.gif "Plugin Video")

## Installation

Similarly to other Flipper plugins for React Native, this one comes in two packages.

### Client package

The first package is a client package that has to be installed in your React Native app.

#### Install the pakage

`npm i rn-flipper-async-storage-advanced --save`

Once the package is installed, simply import it

`import FlipperAsyncStorage from 'rn-flipper-async-storage-advanced';`

and include the component somewhere in you main component, example below adds it inside App.js

```
const App: () => Node = () => {
  const isDarkMode = useColorScheme() === 'dark';

  const backgroundStyle = {
    backgroundColor: isDarkMode ? Colors.darker : Colors.lighter,
  };

  return (
    <SafeAreaView style={backgroundStyle}>
      <FlipperAsyncStorage />  <--- This line
      <TouchableOpacity
        onPress={() => {
          AsyncStorage.setItem('sads', 'das');
        }}>
        <Text>add</Text>
      </TouchableOpacity>
    </SafeAreaView>
  );
};
```

### Flipper plugin

The second package is a plugin package that has to be installed from inside Flipper.

Open Flipper and find your plugin manager, simply search for 'flipper-plugin-async-storage-advanced' and install it.
