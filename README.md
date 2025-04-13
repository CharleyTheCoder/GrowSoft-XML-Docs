# Item Rendering

## Stricture

```xml
<ItemRenderer item="ITEM_ID_CUSTOM_ITEM">
  <Data>
    <!-- Data section for sprites, animations, and particle systems -->
  </Data>

  <RenderRules>
    <!-- Render rules for handling particle systems, sprites, and logic -->
  </RenderRules>
</ItemRenderer>
```

## Data Section

Contains all the visual and particle effects settings for the item

### Sprites

```xml
<Sprite name="spriteName" fileName="filePath" textureSize="textureSize" frame="startFrame,endFrame"/>
```

| Attribute       | Description                                |
|-----------------|--------------------------------------------|
| `name`          | Unique identifier for the sprite           |
| `fileName`      | Path to the texture file                   |
| `textureSize`   | Texture dimensions (e.g., `32`)            |
| `frame`         | Frame range to be used for the sprite      |

### Animations

```xml
<SpriteAnimation name="animationName" sprite="spriteName" animTime="duration">
  <Frame>startFrame,endFrame</Frame>
  <!-- Additional frames here -->
</SpriteAnimation>

<SpriteSinPulseAnimation name="pulseName" sprite="spriteName" autoPlay="true">
  <Parameter name="pos">
    <Set name="period">2000</Set>
    <Set name="scale">3</Set>
  </Parameter>
</SpriteSinPulseAnimation>
```

| Attribute       | Description                                |
|-----------------|--------------------------------------------|
| `name`          | Name of the animation or pulse effect      |
| `sprite`        | Reference to the sprite used in animation  |
| `animTime`      | Duration of the animation in milliseconds |
| `autoPlay`      | If `true`, the animation plays automatically |
| `isLoop`        | If `true`, the animation loops             |
| `period`        | Time period for sine pulse animation      |
| `scale`         | Scale of the sine pulse                    |

~ Written By Charley

[![Discord Presence](https://lanyard.cnrad.dev/api/1248620525035720766)](https://discord.com/users/1248620525035720766)