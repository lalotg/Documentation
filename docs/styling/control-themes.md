# Control Themes
Avalonia 11.0 introduced a new concept called Control Themes. Previously when you wanted to fully re-theme a control you needed to reset every value set in the globally-applied theme. 

## Syntax
Starting from 11.0 Control Themes are used for both Fluent and Simple themes. 
Avalonia team recommends everyone to use Control Themes for defining your themes for the controls for 11.0 and higher.
Let's say we want to create a custom theme for button control based on Fluent Button theme. We are choosing Control Themes in this case because our styles won't leak to other controls because we set Theme's directly for every control.
And control themes only apply to controls which they are directly set to,besides from styles. Styles could be used in Control Themes but they are only applied to the Theme utilizers.
Previously if you would define a Style for the whole app which makes button to be transparent it would apply to all buttons, which may cause unexpected behaviours and style leakage.

To override the theme for control you will need to declare a Theme. Theme is declared in Resources section because ControlTheme is a resource.

When the theme is declared you need to set it as the value for the Control's Theme property.

You can also choose not to declare your theme as a resource, but simply set it directly as the value of the control's Theme property.
