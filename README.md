# &lt;branching-wizard&gt;

> A flexible wizard Polymer element with branches. Branches can be used to have optional wizard-steps or have different flows through your wizard.

## Demo (works best in Chrome)

[Check it live!](http://jns.me/branching-wizard/components/branching-wizard/demo.html)

## How does it work?

A wizard has a certain flow, containing different wizard-steps. In this case the flow is called a *branch*.

The magical part of the branching-wizard element is that it can have multiple branches. This allows you to have optional steps. You can have a different next step depending on a certain choice.

The example below demonstrates a branching-wizard that contains four steps and two branches. In step two, the user can pick a color. The third step will depend on what color the user picked.

The `branch` attribute of the wizard-step determines to what branch the step belongs.
If no branch is set, the step belongs to the *master* branch, which is an empty string.

```HTML
<branching-wizard>
  <wizard-step>
    <h1>Hi, I'm a wizard!</h1>
  </wizard-step>
  <wizard-step>
    <h1>Pick a color:</h1>
    <input type="radio" name="two" value="P" onclick="handleClick(this);">Pink<br />
    <input type="radio" name="two" value="B" onclick="handleClick(this);">Blue
  </wizard-step>
  <wizard-step branch="P" style="color: pink">
    <h2>Her pink nose felt like velvet.</h2>
  </wizard-step>
  <wizard-step branch="B" style="color: skyblue">
    <h2>I'm blue da ba dee da ba die.</h2>
  </wizard-step>
</branching-wizard>
```

```JavaScript
var wizard = document.querySelector('branching-wizard');

var handleClick = function(el){
  wizard.branch = el.value;
};
```

###Validation

What if the user doesn't pick a color? How can you validate user input?
You can listen for the `next` event. Setting the *returnValue* to false will cancel moving to the next step.

```JavaScript
wizard.addEventListener('next', function(e) {
  if(wizard.activeStepIndex == 1){
    if(!wizard.branch)
      e.returnValue=false;
  }
});
```


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
