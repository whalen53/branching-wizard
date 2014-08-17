# &lt;branching-wizard&gt;

> A flexible wizard polymer element with branches. Branches can be used to have optional wizard-steps or have different flows throught your wizard.

## Demo

[Check it live!](http://jns.me/branching-wizard/components/branching-wizard/demo.html)

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install branching-wizard --save
```

## Usage

1. Import Web Components' polyfill:

    ```html
    <script src="bower_components/platform/platform.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/branching-wizard/branching-wizard.html">
    ```

3. Start using it!

    ```html
    <branching-wizard>
        <wizard-step>
          ...
        </wizard-step>
        <wizard-step branch="A">
          ...
        </wizard-step>
        <wizard-step branch="B">
          ...
        </wizard-step>
        <wizard-step>
          ...
        </wizard-step>
    </wizard-wizard>
    ```

See the [component page](http://jns.me/branching-wizard/components/branching-wizard/) for more information.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

Licensed under the MIT license.

Copyright (c) 2014 Wixon.
