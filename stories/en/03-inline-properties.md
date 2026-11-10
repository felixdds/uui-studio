# The Little Cross Beside a Property

[简体中文](../03-inline-properties.md) · English

In UUI Studio's property editor, a property may have a little cross beside it for resetting to the default behavior. It is a small detail, but it illustrates a central choice in UDM: the system needs to know not only what the value is, but whether the user explicitly set it.

## First, a little about UDM

UDM stands for Unified Document Model. It uses a common set of application description rules to organize components, properties, layout, events, state, and related behavior. The build and runtime systems turn those descriptions into DOM, CSS, and JavaScript, rendered through a WebView. Rust handles the host, building, and related platform capabilities.

I want to use established technologies while keeping the designer, property editor, and runtime consistent with the same model. One principle is:

> If something can be derived, do not define it again.

Another is just as important: an explicit decision by the user must be respected.

## Two identical displayed values

Suppose the property editor displays `inherited`. There are two possibilities: the user did not explicitly set the property, and the default or inheritance rules produced that value; or the user explicitly set it to `inherited`.

The displayed value is the same, but the user's intent is different. In the second case, an explicit setting exists, so a reset cross can still appear beside it.

UUI Studio's Form files store explicit settings as inline properties. The value tells the system what was specified; the presence of the corresponding property tells it whether the user explicitly specified anything. There is no need to store another `isDefault` or `isExplicit` flag.

| Situation | Inline setting | Meaning of reset |
| --- | --- | --- |
| No explicit setting | Corresponding property absent | Already computed from default and inheritance rules |
| Explicitly set to inherited | Corresponding property present | Remove the explicit setting and recompute |
| Explicitly set to another value | Corresponding property present | Remove the explicit setting and recompute |

This table describes the semantics, not a new code interface.

## Reset does not mean writing the default value again

When the cross is clicked, Studio removes the corresponding inline property and lets the system recompute the result using its default and inheritance rules. It need not guess whether the user once changed the property, or write the default value at that moment back into the Form.

To me, reducing duplicate definitions means fewer relationships to maintain and fewer opportunities for those relationships to become inconsistent. At the same time, an explicit user setting must not be treated as absent just because it happens to equal the current default.

Behind that little cross is the question of how the model understands user intent.

---

[Series index](README.md) · [Product homepage (Chinese)](../../README.md) · [Previous](02-between-patients.md) · [Next](04-component-responsibilities.md)
