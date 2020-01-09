# My personal HTML convention

## Attribute order (left-to-right):

1. Tag-specific attributes. (eg. anchor's `href=""`, input's `type=""`, label's `for=""`, ...)
2. `id=""`
3. `name=""`
4. Anything not in this list.
5. `placeholder=""`
6. `class=""`
7. Non-value attributes (eg. `required`, `disabled`, ...)

## Class order (left-to-right):

1. Third-parties (eg. bootstrap)
2. Your own classes.

# Examples

## A
```html

<div id="confirmationWindow" class="modal col-12 modal-red">
  <form action="post">
    <summary> Terms and conditions
      <details>Too lazy to post a lorem ipsum, lol.</details>
    </summary>
    <div>
      <label for="confirmTosInput">I accept the <a href="#" class="text-danger">terms and conditions</a></label>
      <input type="checkbox" id="confirmTosInput" name="confirmTosInput" data-special="message" class="form-control" required>
    </div>
</div>
```

