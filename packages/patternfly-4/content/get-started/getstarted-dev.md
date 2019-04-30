---
path: "/get-started/developers"
---
# Develop with PatternFly
Before you begin, check out our [overview of PatternFly 4](/get-started/about) to get acquainted with the basic elements of the design system.

**Before you begin, install a package manager:**

* [Use npm](https://nodejs.org/en/download)
* [Use Yarn](https://yarnpkg.com/en/docs/getting-started)

### Get started with:

* [React](#react)
* [HTML/CSS](#html/css)

## React

The React library provides a collection of React components you can use to build interfaces with consistent markup, styling, and behavior.

## Getting started
  * **Start with a sample project**

  [Start with the PatternFly React seed](#starting-with-the-react-seed). The React seed is an open source build scaffolding utility created to give developers a jump start when creating new projects that will use Patternfly.

  * **Start with your existing project**

  If you want to start with your existing project, skip to the next section, [Installing and configuring PatternFly React](#installing-and-configuring-patternfly).

### Start with the React seed
1. **Fork the project**

  [Fork and clone the PatternFly React Seed project](https://github.com/patternfly/patternfly-react-seed).

  For more information about how to fork and clone a repo, [view GitHub Help](https://help.github.com/articles/fork-a-repo/).


2. **Install the project**

  Follow the steps outlined in the [README](https://github.com/patternfly/patternfly-react-seed#quick-start) to install.

### Install and configure PatternFly React
* Using npm, run the following commands to install:
  ```
  npm install @patternfly/react-core --save
  ```

  **OR**

* Using yarn, run the following commands to install:
  ```
  yarn add @patternfly/react-core
  ```

**Configurations**
* [TypeScript](https://github.com/patternfly/patternfly-react-seed/blob/master/tsconfig.json)
* [Webpack](https://github.com/patternfly/patternfly-react-seed/blob/master/webpack.common.js)
* [Jest](https://github.com/patternfly/patternfly-react-seed/blob/master/jest.config.js)
* [Editor](https://github.com/patternfly/patternfly-react-seed/blob/master/.editorconfig)

## HTML/CSS
The HTML/CSS library provides a collection of code samples you can use to build interfaces with consistent PatternFly markup and styling.

### Install
Using npm, run the following commands to install:
```
npm install @patternfly/patternfly-next
```

**What’s included?**

Each of the three modules (layouts, components, and utilities) delivers a sass file (.scss) and CSS file, so you can include them in your build environment or consume the CSS from your page header.

If you need to overwrite any elements, we recommend extending the variables found in the .scss files, rather than manually overwriting the CSS.

* PatternFly 4 **components** are kept under ``` @patternfly/patternfly-next/components/ ```
* PatternFly 4 **layouts** are kept under ```@patternfly/patternfly-next/layouts/```
* PatternFly 4 **utilities** are kept under``` @patternfly/patternfly-next/utilities/```

**In additional detail, the package includes:**

* A single file for the entire compiled library: ```node_modules/@patternfly/patternfly-next/patternfly.css```

* A minified version of the patternfly.css: ```node_modules/@patternfly/patternfly-next/patternfly.min.css```

* Individual files with each layout,  component, and utility compiled separately:
  * ```node_modules/@patternfly/patternfly-next/layouts/<LayoutName>/<layout-name>.css```
  * ```node_modules/@patternfly/patternfly-next/components/<ComponentName>/<component-name>.css```
  * ```node_modules/@patternfly/patternfly-next/utilities/<UtilityName>/<utility-name>.css```

* A single file for the entire library's source (SASS): ```node_modules/@patternfly/patternfly-next/patternfly.scss```

* Individual source files for each layout, component, and utility (SASS):
  * ```node_modules/@patternfly/patternfly-next/components/<ComponentName>/<component-name>.scss```
  * ```node_modules/@patternfly/patternfly-next/layouts/<LayoutName>/<layout-name>.scss```
  * ```node_modules/@patternfly/patternfly-next/utilities/<UtilityName>/<utility-name>.scss```

Use these files to consume the library. The recommended consumption approach will vary from project to project.

### Configure your project
1. Navigate to the patternfly-next package you just installed and find the PatternFly 4 CSS stylesheet, ```patternfly.css```

2. Copy ```patternfly.css``` to your project's CSS directory.

3. In your HTML file, add the following line to the bottom of your list of CSS files to link to your new stylesheet:

  ```
  <link rel="stylesheet" href="css/patternfly.css">
  ```

  This will ensure that PatternFly 4 styles take precedence over anything that currently resides in your application.

4. If you want to use PatterFly 4 utilities in your project, find the utilities file,  ```patternfly-addons.css```

5. Copy ```patternfly-addons.scss``` into your project’s CSS directory.

6. In your HTML file, add the following line to the bottom of your list of CSS files:

  ```
  <link rel="stylesheet" href="css/patternfly-addons.scss">
  ```

### Using styles
**Typography**

PatternFly 4 uses the Overpass font family. Overpass can be utilized in two different ways:

  * **Built into PatternFly 4**

  By default, Overpass is included as part of the PatternFly 4 distributed CSS file. You do not need to do anything with your configuration to use this font family.

  * **Used as a CDN**

  If you wish to use the CDN for Overpass rather than the default approach, you need to update the ```utilities/variables.scss``` file and build PatternFly 4 as part of your build process.

  To use the CDN vs the standard build, update the ```utilities/variables.scss``` file as follows:

  ```
  $pf-global--enable-font-overpass-cdn: true !default;
  ```

**Icons**

PatternFly 4 uses Font Awesome 5. Font Awesome 5 can be utilized in two different ways:

  * **Built into PatternFly 4**

  By default, Overpass is included as part of the PatternFly 4 distributed CSS file. You do not need to do anything with your configuration to use this font family.

  * **Used as a CDN**

  If you wish to use the CDN for Font Awesome 5 rather than the default approach, you need to update the ```utilities/variables.scss``` file (from source ```node_modules/@patternfly/patternfly-next/```) and build PatternFly 4 as part of your build process.

  To use the CDN vs the standard build, update the ```utilities/variables.scss``` file as follows:

  ```
  $pf-global--enable-fontawesome-cdn: true !default;
  ```

### Customizing PatternFly for your project
The CSS variable system enables you to easily customize things like color or shape without overwriting existing PatternFly styles.

[**Learn more and view CSS variables**](/documentation/react/css-variables/) <i class="blueArrow fas fa-arrow-right pf-u-mx-sm"></i>