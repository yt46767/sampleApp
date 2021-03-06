# Sample App
#### Features
* <a href="https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb">eslint-config-airbnb</a>
* <a href="https://github.com/reactjs/react-redux">Redux</a> (
  <a href="https://github.com/gaearon/redux-thunk">redux-thunk</a>, redux-logger)
* <a href="https://facebook.github.io/immutable-js/">Immutable.js</a>
* <a href="https://github.com/aksonov/react-native-router-flux">react-native-router-flux</a>
* <a href="https://facebook.github.io/jest/">Jest</a> snapshot tests. (components only now, work in progress)
* <a href="https://github.com/erikras/redux-form">redux-form</a>
#### Description

React Native boilerplate with authorization (redux-form validation) and persistent login.

<p align="center">
  <img src="./demo.gif" width="300"/>
</p>

### Installation
- <b>Mobile App</b>

  Clone the repository and run the following commands under your project root:
  Must have react-native installed. (https://facebook.github.io/react-native/docs/getting-started.html)
  ```
  npm i
  ```
  Connect a device or use virtual device (https://www.genymotion.com/) and run:
  ```
  react-native run-android
  react-native start
  ```
- <b>Server</b>

  Navigate to sampeServer folder.
  Run the following commands in sampleServer folder:
  ```
  npm i
  node server.js
  ```
  <b>Change apiEndpoint in root/app/urls.js to match server address</b>


------------------------------------------------------------------------------------
ytao

词汇：
--------------
authentication
鉴别、证明

profile
介绍

路由走向：
(核心：react-native-router-flux)
---------------------------------

----index.js
      <Provider store={store}>
        <AppRoot />
      </Provider>

----AppRoot.react.js
      <RouterWithRedux scenes={scenes} />

----scenes.js
      const scenes = Actions.create(
      <scene key="root">
        <scene key="splash">

        </scene>
        <scene key="rootTabbar">

        </scene>
        <scene key="homeTab">

        </scene>
        <scene key="profileTab">

        </scene>
        <scene key="authentication">

        </scene>
      </scene>
      )
      export default scenes;

模块说明：
-----------------------------------
------加载模块
        splashscreen/SplashScreen.react.js

