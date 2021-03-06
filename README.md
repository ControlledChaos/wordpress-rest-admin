## WordPress REST Admin

A frontend for admin area of WordPress, using [WP REST API](https://v2.wp-api.org/) and [React](https://reactjs.org/).
It works with Self-Hosted WordPress.

[![Alt Screenshot](https://user-images.githubusercontent.com/20383976/41827852-a5e8504c-77e6-11e8-8667-3eb80f910fa2.png)](https://vimeo.com/276794147)

This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app).

## Features

- Login (using JWT WP REST Plugin)
- Dashboard
- Posts(List, Edit, Add New, Trash)
- Pages(List, Edit, Add New, Trash)
- Categories and Tags
- Comments
- Users
- Profile
- Settings

## Usage

### Backend - what needs to be done first
Make sure you have WP REST API and JWP plugin installed in your wordpress
#### WP REST API
- https://v2.wp-api.org/
- Note that WordPress (4.7 or later) has this installed by default

#### JWP Authentication for WP REST API 
- [Installation instructions](https://wordpress.org/plugins/jwt-authentication-for-wp-rest-api/)
- [Tutorial](https://www.youtube.com/watch?v=Mp7T7x1oxDk)

### git clone and npm start
- Run these commands just to see how it works
```
git clone https://github.com/rnaga/wordpress-rest-admin.git .
npm install
npm start
```
- Visit http://localhost:3000

### Use as a React Component

- Create a new React project with [Create React App](https://github.com/facebook/create-react-app)
- Import package
```
cd /path/to/your/project
npm install
npm i wordpress-rest-admin
```
- and render it
```
import WPAdmin from 'wordpress-rest-admin/WPAdmin';
import contents from 'wordpress-rest-admin/contents';
import loginLogo from './WordpressLogo.svg';
import headerLogo from './WordpressLogo.png';

...

<WPAdmin
  loginLogo={loginLogo}
  headerLogo={headerLogo}
  defaultContent={defaultContent}
  contents={contents}
/>
```
See example [here](https://github.com/rnaga/wordpress-rest-admin/tree/master/example)

## Supported Browsers

By default, the generated project uses the latest version of React.

You can refer [to the React documentation](https://reactjs.org/docs/react-dom.html#browser-support) for more information about supported browsers.

