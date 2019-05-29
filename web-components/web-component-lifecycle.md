# Web Component Lifecycle

A custom element can define special lifecycle hooks for running code during interesting times of its existence. These are called custom element reactions.

| Name     | Called when      
|----------|-----------
| constructor() | An instance of the element is created or upgraded. Useful for initializing state, settings up event listeners, or creating shadow dom.
| connectedCallback() | Called every time the element is inserted into the DOM. Useful for running setup code, such as fetching resources or rendering. Generally, you should try to delay work until this time.
| disconnectedCallback() | Called every time the element is removed from the DOM. Useful for running clean up code.
| attributeChangedCallback() | Called when an observed attribute has been added, removed, updated, or replaced. Also called for initial values when an element is created by the parser, or upgraded. Note: only attributes listed in the observedAttributes property will receive this callback.
| adoptedCallback() | The custom element has been moved into a new document (e.g. someone called document.adoptNode(el)).

[developers.google.com](https://developers.google.com/web/fundamentals/web-components/customelements)