# projectwater

A short VR music + dance experience.

> _it's giving dance_ 💃

![image](https://github.com/quinnouyang/projectwater/assets/90884224/7e7c1a4f-20fb-414e-9e7c-d65cc0c5ceac)

# Development

> Some development rambles/notes from Quinn as he struggles with Unity. Mostly dumbed down from the [XR toolkit docs](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.3/manual/index.html) and [VR template docs](https://docs.unity3d.com/Packages/com.unity.template.vr@8.0/manual/index.html).

## Interactivity

### [Interaction States](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.3/manual/architecture.html)

There are interactables (e.g. manipulatable in-game objects) and interactors (e.g. user peripherals/controls). With both of these, there are three states: hover, select, and activate; these are synonmous with mouseover, mousedown, and another mousedown (further interaction after select/mousedown).

### [Affordance System](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.3/manual/affordance-system.html)

> "In psychology, affordance is what the environment offers the individual"

"Enables users to create visual and auditory feedback to interaction states." Oversimplified information flow:
1. Interactable (Affordance State Provider) reads the current interaction state
2. Interaction state fires to the three affordance state receivers: audio, color material property, and uniform transform scale affordance (???) receivers.
3. Each receiver refers to an Affordance Theme to determine their event behavior, which can "also be configured locally on the component itself." (???)

## Animation

An [Animation Controller](https://docs.unity3d.com/Manual/class-AnimatorController.html) encapsulates animation behaviors which we can then attach to an object. I'm sure it has more general purposes but since we're stupid, let the object be the avatar of which we have an animation clip recorded.

### Basic Looped Animation
1. Create an Animation Controller asset and open it in the Animator
2. Drag and drop an animation clip, usually packaged under a model if it's an FBX
3. Right-click the Entry state, select "Make Transition," and select the animation clip.
4. Repeat 3. but start and end at the same animation clip (this loops).

![image](https://github.com/quinnouyang/projectwater/assets/90884224/10a6a7f9-276e-4240-af54-e2f5af240a53)

Drag a model to the Scene and then an Animation Controller on top of it.

## Acknowledgements

- John Toenjes - For directing DANC 426
- Mari Yamashita - For dancing the night away
- Lucas Santois - For his project management
- Kris Huang - For their color palette
- And the rest of DANC 426 for tolerating our music shenanigans...
