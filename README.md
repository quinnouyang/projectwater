# projectwater

_it's giving dance_ 💃

# Development

> Mainly rambles from Quinn as he struggles to learn game development and curses at C#...
> 
> Mostly dumbed down from the [XR toolkit docs](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.3/manual/index.html) and [VR template docs](https://docs.unity3d.com/Packages/com.unity.template.vr@8.0/manual/index.html).

## Interactivity

### [Interaction States](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.3/manual/architecture.html)

There are interactables (e.g. manipulatable in-game objects) and interactors (e.g. user peripherals/controls). With both of these, there are three states: hover, select, and activate; these are synonmous with mouseover, mousedown, and another mousedown (further interaction after select/mousedown).

### [Affordance System](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.3/manual/affordance-system.html)

> "In psychology, affordance is what the environment offers the individual"

"Enables users to create visual and auditory feedback to interaction states." Oversimplified information flow:
1. Interactable (Affordance State Provider) reads the current interaction state
2. Interaction state fires to the three affordance state receivers: audio, color material property, and uniform transform scale affordance (???) receivers.
3. Each receiver refers to an Affordance Theme to determine their event behavior, which can "also be configured locally on the component itself." (???)
