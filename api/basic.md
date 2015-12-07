# RWR
* js:
    * [registerComponent](./basic.html#js-registercomponent)
    * [getComponent](./basic.html#js-getcomponent)
    * [createComponent](./basic.html#js-createcomponent)
    * [renderComponent](./basic.html#js-rendercomponent)
    * [unmountComponent](./basic.html#js-unmountcomponent)
* ruby: 
    * [react_component](./basic.html#ruby-reactcomponent)


---


* #### [js] registerComponent
  ```js
  registerComponent(String componentName, class|function component)
  ```

  Register component so it's globally accessible.

  ##### example:

  ```js
  import MyComponent from 'my-component';

  RWR.registerComponent('MyComponentName', MyComponent);
  ```

  **note:** Registered components are accessible in globally exposed `ReactRailsUJS` under `reactComponents` property.

* #### [js] getComponent

  ```js
  getComponent(String componentName)
  ```

  Shortcut for accessing registered component.

  ##### example:

  ```js
  RWR.getComponent('MyComponentName');
  ```

* #### [js] createComponent

  ```js
  createComponent(String componentName[, Object props])
  ```

  Wrapper over React.createElement that creates ready to render component with props.

  ##### example:

  ```js
  RWR.createComponent('MyComponentName', {foo: 'bar'});
  ```

* #### [js] renderComponent

  ```js
  renderComponent(String componentName, Object props, DOMElement container)
  ```

  Wrapper over `React.render` and `React.createElement`. Renders component with given props into specified DOM element.

  ##### example:

  ```js
  var element = document.getElementById('my-element');
  RWR.renderComponent('MyComponentName', {foo: 'bar'}, element);
  ```

* #### [js] unmountComponent

  ```js
  unmountComponent(DOMElement container)
  ```

  Wrapper over `React.unmountComponentAtNode`. It will unmount component from given DOM node.

  ##### example:

  ```js
  var element = document.getElementById('my-element');
  RWR.unmountComponent(element);
  ```

* ### [ruby] react_component

  ```ruby
  react_component(String component_name[, Object props])
  ```

  Creates DOM node with props as data attributes in rendered view so ReactRailsUJS can grab it and mount proper  component.

  ##### example:

  ```ruby
  <%= react_component('MyComponentName', MySerializer.new(my_data)) %>
  ```

  **note:** Props Object will be parsed to JSON. Be careful when passing rails models there - all its data accessible after `.to_json` will be exposed as data-attributes. We  recommend using serializers to control it.
