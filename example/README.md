# Usage

```
npm install
npm i wordpress-rest-admin
npm start
```
# App.js
```
import React, { Component } from 'react';
import WPAdmin from 'wordpress-rest-admin/WPAdmin'; 
import contents from 'wordpress-rest-admin/contents';
import loginLogo from './WordpressLogo.svg';
import headerLogo from './WordpressLogo.png';

class App extends Component {

    render() {

        // Retrieve contents 
        const {dashboard, posts, pages, categories, tags, comments, users, profile, settings} = contents;

        // Set default content
        const defaultContent = dashboard;


        return (<WPAdmin 
          loginLogo={loginLogo}
          headerLogo={headerLogo}
          defaultContent={defaultContent}
          contents={{dashboard, posts, pages, categories, tags, comments, users, profile, settings}} 
        />);
    }
}

export default App;
```
