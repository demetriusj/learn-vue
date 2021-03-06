### What is Vuejs?

Its a javascript framework & tool to build single page applications (SPA).

What is a SPA and why should we care?

- Vue supports SSR (for SEO & Performance)
- Documentation @ vuejs.org
- MIT license
- Good Ecosystem 75K stars
- Limited support for IE8 below
- Opinionated State Management and Routing
- Other frameworks React, EmberJS, Angular, PolymerJS

### Vue Tools

Vue includes tools to compile, bundle, debug, and package your application.
When using vue its helpful to under stand the tooling and the framework.
Not only does vue rely on build tools it use transpilers in the build phase
to convert template into javascript like JSX.

### Vue Framework

[Diagram]: https://vuejs.org/images/data.png "Diagram"

Vue is template based. Letting you define the markup with HTML.
Additionally you can use directive to add interpolation so
your application state can drive your UI directly.

- Drop-in & build-time bundle
- Build-in features
    - routing
    - testing
    - components
    - etc.

### State Management

Vue relies on a type of data binding similar to MVVM
to support reactive views. It differs from react because
React is closer to a MVC based system. React is only the
view layer and lets redux/MobX/etc to handle application state.

With reactive views the side effects are controlled directly by
watching changes to the model and the view can read/write directly
to the model without going through a controller.

![Diagram](https://upload.wikimedia.org/wikipedia/commons/8/87/MVVMPattern.png)

### Docs

- [API](https://vuejs.org/v2/api/)
- [Template](https://vuejs.org/v2/guide/syntax.html#Raw-HTML)

### Template Syntax

The template are based on .vue files and inline markup.
The .vue files are converted into javascript via build
step. The template support:

- Styles via PostCSS
- ES5/ES6
- Interpolations
- Spec-compliant HTML
- Directives
- Components

# Following the lesson
The `step` can be step1, step2, ... step5

```
$git reset --hard `step` && git clean -f -d
```

# Make todo app

STEP 1: [Setup the tooling](./docs/setup.md)

VERIFY: [Run the basic template](./docs/run-it.md)

STEP 2: [Build the basic application foundation](./docs/basic-app.md)

STEP 3: [Todo List](./docs/binding.md)

STEP 4: [Edit Todo](./docs/editing.md)

STEP 5: [Style](./docs/style.md)
