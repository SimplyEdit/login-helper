# login-helper
Makes it easier to start SimplyEdit

## Usage
checkout this git repository into your javascript assets directory, e.g.

```
  cd www/js/
  git clone https://github.com/simplyedit/login-helper
```

Then include the login helper in your html, like this:

```
  <body>
    ...
    <script src="/js/login-helper/simplyedit-helper.js"></script>
  </body>
</html>
```

And you're done. The login helper will detect when you start SimplyEdit for the first time on a specific browser. After that it will show a SimplyEdit button in the bottom right of the website, whenever you return to it. Pressing the button will start SimplyEdit on that page.

You can remove the button by pressing it and holding it for a second. The button will remain gone, untill you start SimplyEdit by hand - by adding `#simply-edit` to the URL - again.

## Customization

By default the helper button starts at 50px from the bottom and from the right. You can change this by changing the localStorage variable `helper`:

```
  localStorage.setItem('simplyEditLoginHelper', {
    x: 50,
    y: 50
  });
```
This enables the helper button and sets its position to 50px from the top and left. Negative values position it from the bottom and right.

## Branding

You can change the entire style and content of the login button, by including an HTML element with a specific ID in your HTML:

```
  <body>
    ...
    <div style="visibility: hidden;" id="SimplyEditLogin">My Login</div>
    ...
    <script src="/js/login-helper/simplyedit-helper.js"></script>
  </body>
</html>
```

The login helper javascript will detect this element and add the login helper behaviour to it, without changing its contents, style or position. You should make sure the element is hidden by default.

