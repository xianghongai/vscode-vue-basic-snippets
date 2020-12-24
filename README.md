<p>
  <h1 align="center">Vue Basic Snippets (Visual Studio Code)</h1>
</p>

<p align="center">
  <a href="https://github.com/xianghongai/vscode-vue-basic-snippets">
    <img src="https://img.shields.io/github/repo-size/xianghongai/vscode-vue-basic-snippets?style=plastic&color=4ac51c">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-vue-basic-snippets">
    <img src="https://vsmarketplacebadge.apphb.com/version-short/NicholasHsiang.vscode-vue-basic-snippets.svg?style=plastic&color=f07b3c">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-vue-basic-snippets">
    <img src="https://vsmarketplacebadge.apphb.com/installs-short/NicholasHsiang.vscode-vue-basic-snippets.svg?style=plastic&color=4ac51c">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-vue-basic-snippets">
    <img src="https://vsmarketplacebadge.apphb.com/rating-short/NicholasHsiang.vscode-vue-basic-snippets.svg?style=plastic&color=4ac51c">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-vue-basic-snippets">
    <img src="https://img.shields.io/github/license/xianghongai/vscode-vue-basic-snippets?maxAge=2592000&style=plastic&color=4ac51c">
  </a>
</p>

[中文](./README_CN.md)

🌈🌈🌈 Need to install "[Vue 2 Snippets](https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-vue2-snippets)" **or** "Vue 3 Snippets" (coming soon), **they are one combined release.**

## Design

![DESIGN](https://raw.githubusercontent.com/caringrun/assets/master/vscode-vue-snippets.png)

Vue 2 and 3 have relatively large changes, 2 recommends the Optional paradigm, and 3 recommends the Composition Functions paradigm. The commonly used "Global API, Directives, Transition, Async Components, Instance Events, Lifecycle" in Vue have undergone major changes. And VueX also launched 4 versions.

In addition, with the introduction of new features of "reactive refs" and "Teleport", the upgrade of many community resources will be major changes.

Therefore, it is not good to design Vue 2 and 3 Code Snippets together.

It is best to separate the Code Snippets of Vue 2 and 3 respectively. According to the actual situation in the project, select `Disable (Workspace)` in the extension. If you feel this is more cumbersome, you can install the extension supported by version 2 in "`VS Code`" , Install the extensions supported by version 3 in "`VS Code-Insiders`".

Vue 2 and 3 Template Directives are the same.

---

![](https://raw.githubusercontent.com/caringrun/assets/master/vscode-vue-html-snippets.gif)

## Supported languages (file extensions)

- HTML (`.html`)
- HTML (`.vue`)
- JavaScript (`.js`)
- TypeScript (`.ts`)
- Vue (`.vue`)

## Resources 🤞

- [JavaScript Code Snippet - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-javascript-snippet)
- [JavaScript Comment Snippet - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-javascript-comment)
- [React Snippets - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=NicholasHsiang.vscode-react-snippet)

## Snippets

- HTML
    * Style & Class
    * Directives
    + Dynamic Component, Keep Alive
    + Slot
    * Transition
    * Instance Methods Events
    * Vue Router
- CSS
- JavaScript


### HTML 🌴

#### Style & Class

- `vClass` - `:class="{ 'class-name': expression }"`, Class binding: object syntax inline
- `vClass` - `:class="classObject"`, Class binding: object syntax
- `vClass` - `:class="[classObject]"`, Class binding: apply a list of classes
- `vClass` - `:class="[expression ? 'class-name' : '', classObject]"`, Class binding: with a ternary expression
- `vClass` - `:class="[classObject, { 'class-name': expression }]"`, Class binding: multiple conditional classes
- `vStyle` - `:style="{ 'css-property': 'value', cssProperty: `${styleValue}px` }"`, Style binding: object syntax inline
- `vStyle` - `:style="styleObject"`, Style binding: object syntax
- `vStyle` - `:style="[baseStyles, overridingStyles]"`, Style binding: multiple styles

#### Directives

- `template` - template
- `templateFunctional` - functional template
- `xtemplate` - x-template
- `vFor` - `v-for="(item, index) in items" :key="index"`, Vue v-for
- `vForWithoutKey` - `v-for="item in items"`, Vue v-for, Without Key
- `vIf` - `v-if="condition"`, Vue v-if
- `vElse` - `v-else`, Vue v-else
- `vElseIf` - `v-else-if="condition"`, Vue v-else-if
- `vIfWithKey_UNSAFE` - `v-if="condition" key="{feature}"`, Vue v-if, With Key, **Vue 3 DEPRECATED!**
- `vElseWithKey_UNSAFE` - `v-else key="{feature}"`, Vue v-else, With Key, **Vue 3 DEPRECATED!**
- `vElseIfWithKey_UNSAFE` - `v-else-if="condition" key="{feature}"`, Vue v-else-if, With Key, **Vue 3 DEPRECATED!**
- `vShow` - `v-show="condition"`, Vue v-show
- `vText` - `v-text="text"`, Vue v-text
- `vFilter_UNSAFE` - `:text-content.prop="text | filter"`, Vue v-bind filter, **Vue 3 REMOVED!**
- `vHtml` - `v-html="html"`, Vue v-html
- `vModel` - `v-model="value"`, Vue v-model
- `vOn` - `@click="handler(arg, $event)"`, v-on event/listener
- `vOnLonghand` - `v-on:click="handler(arg, $event)"`, v-on Longhand
- `vOnDynamic` - `@[event]="handler(arg, $event)"`, v-on dynamic event
- `vOnStopPropagation` - `vOnStopPropagation`, v-on stop propagation
- `vOnPreventDefault` - `@click.prevent="handler(arg, $event)"`, v-on prevent default
- `vOnStopPropagationPreventDefault` - `@click.stop.prevent="handler(arg, $event)"`, v-on stop propagation and prevent default
- `vOnKeyAlias` - `@keyup.enter="handler(arg, $event)"`, v-on key modifier using keyAlias
- `vOnKeyCode_UNSAFE` - `@keyup.13="handler(arg, $event)"`, v-on key modifier using keyCode, **Vue 3 DEPRECATED!**
- `vOnOnce` - `@click.once="handler(arg, $event)"`, v-on triggered at most once
- `vOnObject` - `v-on="{ mousedown: handler(arg, $event), mouseup: handler(arg, $event) }"`, v-on object syntax
- `vBind` - `:attribute="value"`, Vue v-bind
- `vBindLonghand` - `v-bind:attribute="value"`, Vue v-bind Longhand
- `vBindDynamic` - `:[attribute]="value"`, Vue v-bind dynamic directive
- `vAttrs` - `"v-bind="$attrs"`, Vue v-bind $attrs
- `vOnce` - `v-once `, Vue v-once
- `vPre` - `v-pre `, Vue v-pre
- `vCloak` - `v-cloak `, Vue v-cloak
- `vEmit` - `@event="$emit('event-name', $event.target.value)"`, $emit
- `ref` - `ref="reference"`
- `key` - `:key="number|string|boolean|symbol"`

#### Dynamic Component

- `component` - `<component :is="componentId"></component>`
- `keepAlive` - `<keep-alive></keep-alive>`

#### Slots

- `slotElement` - `<slot>` Element
- `slotElementScope` - `<slot>` Element, Scoped Slots
- `vSlot` - v-slot
- `vSlotScope` - v-slot, Scoped Slots
- `vSlotLonghand` - v-slot, Longhand
- `vSlotScopeLonghand` - v-slot, Scoped Slots, Longhand
- `UNSAFE_slot` - UNSAFE!!! Slot Deprecated
- `UNSAFE_slotScope` - UNSAFE!!! Slot Deprecated, Scope Removed
- `UNSAFE_slotSlotScope` - UNSAFE!!! Slot Deprecated, slotScope Deprecated

#### Transitions

- `transition` - Vue Transition Component
- `transition` - Vue Transition Component with JavaScript Hooks
- `transitionGroup` - Vue transition-group Component

##### Custom Transition Classes

- `enterClass` / `transitionEnterClass` - enter-class
- `enterActiveClass` / `transitionEnterActiveClass` - enter-active-class
- `enterToClass` / `transitionEnterToClass` - enter-to-class
- `leaveClass` / `transitionLeaveClass` - leave-class
- `leaveToClass` / `transitionLeaveToClass` - leave-to-class
- `leaveActiveClass` / `transitionLeaveActiveClass` - leave-active-class
- `appearClass` / `transitionAppearClass` - appear-class
- `appearToClass` / `transitionAppearToClass` - appear-to-class
- `appearActiveClass` / `transitionAppearActiveClass` - appear-active-class

##### Hooks

- `beforeEnterHook`/`transitionBeforeEnterHook` → `@before-enter='beforeEnter'`
- `enterHook`/`transitionEnterHook` → `@enter='enter'`
- `afterEnterHook`/`transitionAfterEnterHook` → `@after-enter='afterEnter'`
- `enterCancelledHook`/`transitionEnterCancelledHook` → `@enter-cancelled='enterCancelled'`
- `beforeLeaveHook`/`transitionBeforeLeaveHook` → `@before-leave='beforeLeave'`
- `leaveHook`/`transitionLeaveHook` → `@leave='leave'`
- `afterLeaveHook`/`transitionAfterLeaveHook` → `@after-leave='afterLeave'`
- `leaveCancelledHook`/`transitionLeaveCancelledHook` → `@leave-cancelled='leaveCancelled'`
- `beforeAppearHook`/`transitionBeforeAppearHook` → `@before-appear='beforeAppear'`
- `appearHook`/`transitionAppearHook` → `@appear='appear'`
- `afterAppearHook`/`transitionAfterAppearHook` → `@after-appear='afterAppear'`
- `appearCancelledHook`/`transitionAppearCancelledHook` → `@appear-cancelled='appearCancelled'`


#### Vue Router

- `routerView` - `<router-view></router-view>`, Router View;
- `routerViewNamed` - `<router-view name="viewFeature"></router-view>`, Named Router View;
- `routerLink` - `<router-link to="">path</router-link>`, Router link with literal string;
- `routerLink` - `<router-link :to="">path</router-link>`, Router link using v-bind;
- `routerLinkPath` - `<router-link :to="{ path: 'pathname' }">pathname</router-link>`, Router link to path;
- `routerLinkParams` - `<router-link :to="{ path: 'pathname', params: { property: 'value' } }">path</router-link>`, Router link to path with params;
- `routerLinkQuery` - `<router-link :to="{ path: 'pathname', query: { property: 'value' } }">path</router-link>`, Router link to path with query;
- `routerLinkAppend` - `<router-link :to="{ path: 'pathname' }" append>path</router-link>`, Router link to path using append mode;
- `routerLinkReplace` - `<router-link :to="{ path: 'pathname' }" replace>path</router-link>`, Router link to path using replace mode;
- `routerLinkNamedRoute` - `<router-link :to="{ name: 'routename' }">path</router-link>`, Router link to named route;
- `routerLinkNamedRouteParams` - `<router-link :to="{ name: 'routename', params: { property: 'value' } }">path</router-link>`, Router link to named route with params;
- `routerLinkNamedRouteQuery` - `<router-link :to="{ name: 'routename', query: { property: 'value' } }">path</router-link>`, Router link to named route with query;
- `routerParams` - `params: { property: 'value' }`, Router with params;
- `routerQuery` - `query: { property: 'value' }`, Router with query;
- `routerActiveClass` - `active-class="router-link-active"`, Router active-class;
- `routerExact` - `exact`, Router with exact match;
- `routerExactActiveClass` - `exact-active-class="router-link-exact-active"`, Router exact-active-class;
- `routerAriaCurrentValue` - `aria-current-value="page"`, Router aria-current-value;
- `routerTag` - `tag="a"`, Router tag;


### CSS 🌷

- `v-cloak`
- `enterCSS`/ `transitionEnterCSS`  → `.feature-enter {}`
- `enterActiveCSS`/`transitionEnterActiveCSS`  → `.feature-enter-active {}`
- `enterToCSS`/ `transitionEnterToCSS`  → `.feature-enter-to {}`
- `leaveCSS`/ `transitionLeaveCSS`  → `.feature-leave {}`
- `leaveToCSS`/ `transitionLeaveToCSS`  → `.feature-leave-to {}`
- `leaveActiveCSS`/`transitionLeaveActiveCSS`  → `.feature-leave-active {}`
- `appearCSS`/ `transitionAppearCSS`  → `.feature-appear {}`
- `appearToCSS`/ `transitionAppearToCSS`  → `.feature-appear-to {}`
- `appearActiveCSS`/`transitionAppearActiveCSS`  → `.feature-appear-active {}`


### JavaScript 🌿

#### Transition

- `beforeEnterEvent` / `transitionBeforeEnterEvent` - before-enter
- `enterEvent` / `transitionEnterEvent` - enter
- `afterEnterEvent` / `transitionAfterEnterEvent` - after-enter
- `enterCancelledEvent` / `transitionEnterCancelledEvent` - enter-cancelled
- `beforeLeaveEvent` / `transitionBeforeLeaveEvent` - before-leave
- `leaveEvent` / `transitionLeaveEvent` - leave
- `afterLeaveEvent` / `transitionAfterLeaveEvent` - after-leave
- `leaveCancelledEvent` / `transitionLeaveCancelledEvent` - leave-cancelled
- `beforeAppearEvent` / `transitionBeforeAppearEvent` - before-appear
- `appearEvent` / `transitionAppearEvent` - appear
- `afterAppearEvent` / `transitionAfterAppearEvent` - after-appear
- `appearCancelledEvent` / `transitionAppearCancelledEvent` - appear-cancelled


## License 📃

MIT License

---

**Donate**

![xianghongai@gmail.com](https://raw.githubusercontent.com/caringrun/assets/master/donate.png)
