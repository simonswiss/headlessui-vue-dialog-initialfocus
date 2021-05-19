## Dialog (Vue) bug repro

When setting the `:initialFocus` attribute to the `Dialog` component, the cycling through focusable elements within the dialog stop working. Focus is "trapped" on the element with the `initialFocus` ref, and not moving to anything else.

Same setup without the `initialFocus` attribute applied cycles through the buttons as expected.
