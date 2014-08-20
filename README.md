# &lt;branching-wizard&gt;

> A flexible wizard Polymer element with branches. Branches can be used to have optional wizard-steps or have different flows through your wizard.

## Demo (Works best in Chrome)

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

## Author

[Jonas Anseeuw](http://jns.me)

## License

Copyright © 2014 Jonas Anseeuw

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
