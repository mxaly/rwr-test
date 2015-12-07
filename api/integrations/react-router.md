# RWR.reactRouter

* js:
    *  [registerRouter](./integrations/js-reactrouter)
    *  [getRouter](./integrations/js-getrouter)
    *  [renderRouter](./integrations/js-renderrouter)
* ruby:
    *  [react_router](./integrations/ruby-reactrouter)

---



* #### [js] registerRouter
  ```js
  registerRouter(String routerName, class|function component)
  ```

  Register router so it's globally accessible.

  ##### example:

  ```js
  import MyComponent from 'my-component';

  RWR.reactRouter.registerComponent('MyComponentName', MyComponent);
  ```

  **note:** Registered components are accessible in globally exposed `ReactRailsUJS` under `reactRouters` property.

* #### [js] getRouter

  ```js
  getRouter(String routerName)
  ```

  Shortcut for accessing registered router.

  ##### example:

  ```js
  RWR.reactRouter.getRouter('MyRouterName');
  ```

* #### [js] renderRouter

  ```js
  renderRouter(String routerName, Object props, DOMElement container)
  ```

  TODO
  
* #### [ruby] react_router

  ```ruby
  react_router(String router_name)
  ```

  ##### example:

  ```ruby
  <%= react_router('MyRouterName') %>
  ```