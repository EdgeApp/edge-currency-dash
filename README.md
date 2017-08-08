# Airbitz Dash Currency Plugin

Implement Dash transactions using the Airbitz currency plugin API
The API can be found [here](https://developer.airbitz.co/javascript/#currency-plugin-api)

## Installing

Since this package is not on NPM, you will have to do things manually:

1. Clone this project into a directory next to your project.
2. Add to your project's `package.json`:

    ```
    cd ../your-project
    npm install git+ssh://git@github.com/Airbitz/airbitz-currency-dash.git
    ```
## Usage

Initialize the plugin:

```
import { DashPlugin } from `airbitz-currency-dash`

DashPlugin.makePlugin({
  io: yourPlatformSpecifcIo
}).then(dashPlugin => {

})
```

Now you can pass `dashPlugin` to `airbitz-core-js`.

    
## Developing the library

1. Install cli-tool, dependencies, & build the library:

    ```
    git clone git@github.com:Airbitz/airbitz-cli.git
    git clone git@github.com:Airbitz/airbitz-cli-react-native.git
    git clone git@github.com:Airbitz/airbitz-currency-dash.git
    cd airbitz-currency-dash
    npm install
    cd airbitz-cli
    npm install
    cd airbitz-cli-react-native
    npm install
    npm run updot
    ```

Updot is a tool to copy needed files from peer dependencies into the node_modules of the project it is run in. This replaces the need for `npm link` which is broken in React Native.

Launch the xcode project in `airbitz-cli-react-native/ios` to launch the cli tool. CLI command documentation can be seen by running `airbitz-cli help` from within the `airbitz-cli` project directory.
