# ES5+ Workflow
* Template workflow to creating ES5+ applications without the hassle of going through the webpack and babel setup every time.

* Included Dependencies:
    * Babel and webpack to translate ES5+ code into legacy-compatible code for older browsers and local webserver.
    * HTML, CSS, and image handling dependencies to correctly generate templates.

## Installation Instructions:
1. Clone this repository:
    `git clone https://github.com/nchan9/js-workflow.git`

2. Install dependencies:
    `npm install`

3. Generate dist and node_modules folders:
    `npm run dev` or `npm dev`

4. Run the webpack server to verify successful installation. This should open a browser window that displays "hello world" in red.
    `npm start`
5. That's it! You're ready to start your project!

## Basic Template Reference
* To add additional HTML templates, CSS stylesheets, or JS scripts, include them in `/src`. Run the scripts to update in `/dist`.
* To properly generate HTML templates in the `/dist` directory, duplicate the existing code block within the plugins setting in the `webpack.config.js` file. For example, if I wanted to add an additional HTML file named `about.html`, your plugins config should look like this:
    ```
    plugins: [
        new HtmlWebpackPlugin({
            filename: 'index.html',
            template: './src/index.html'
        }),
        new HtmlWebpackPlugin({
            filename: 'about.html',
            template: './src/about.html'
        })
    ],
    ```
* For a full reference, see the full plugin [documentation](https://webpack.js.org/plugins/html-webpack-plugin/).

## Optional 
* Customize project info in package.json
* Install additional dependencies and add additional configuration settings in `webpack.config.json`