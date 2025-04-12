# GrowSoft-XML-Docs

## Particle Systems

Particle systems in Growtopia's custom `ItemRenderer` XMLs define animated visual effects like sparkles, orbits, and glows. Each system contains an `<Emitter>` and a `<Particle>` section.

### Basic Structure

```xml
<ParticleSystem name="uniqueParticleName">
  <Emitter>
    <Set name="offset">0, -16</Set>
    <Set name="emissionInterval">0.8</Set>
    <Set name="infParticles">true</Set>
    <Set name="infLifeTime">true</Set>
    <Set name="particlesPerEmission">1</Set>
    <OrbitOffset>
      <Set name="hasOrbit">true</Set>
      <Set name="hOrbitPeriod">6000</Set>
      <Set name="hAmplitude">20</Set>
      <Set name="vOrbitPeriod">4000</Set>
      <Set name="vAmplitude">12</Set>
      <Set name="hTimeOffset">0</Set>
      <Set name="vTimeOffset">0</Set>
      <Set name="minScale">0.5</Set>
      <Set name="maxScale">1</Set>
    </OrbitOffset>
  </Emitter>
  <Particle>
    <Set name="sprite">spriteName</Set>
    <Set name="relativeToEmitter">true</Set>
    <Set name="inSpecificOrder">true</Set>
    <Set name="blendingMode">PREMULTIPLIED_ALPHA</Set>
    <Set name="lifeTime">0.9</Set>
  </Particle>
</ParticleSystem>```

### Emitter Settings

| Setting               | Description                                 |
|-----------------------|---------------------------------------------|
| `offset`              | Position offset from the player (x, y)      |
| `emissionInterval`    | Seconds between particle spawns             |
| `infParticles`        | If true, spawns particles infinitely        |
| `infLifeTime`         | Particles don’t expire over time            |
| `particlesPerEmission`| Number of particles emitted at once         |

### OrbitOffset (Optional)

| Setting         | Description                              |
|-----------------|------------------------------------------|
| `hasOrbit`      | Enables orbit motion                     |
| `hOrbitPeriod`  | Horizontal orbit duration (ms)           |
| `hAmplitude`    | Horizontal range of orbit                |
| `hTimeOffset`   | Delays start of horizontal motion        |
| `vOrbitPeriod`  | Vertical orbit duration (ms)             |
| `vAmplitude`    | Vertical range of orbit                  |
| `vTimeOffset`   | Delays start of vertical motion          |
| `minScale`      | Smallest scale during animation          |
| `maxScale`      | Largest scale during animation           |

### Particle Settings

| Setting              | Description                                      |
|----------------------|--------------------------------------------------|
| `sprite`             | The sprite to render                             |
| `relativeToEmitter`  | If true, particle stays relative to emitter      |
| `inSpecificOrder`    | Forces specific spawn order                      |
| `blendingMode`       | Usually `PREMULTIPLIED_ALPHA`                    |
| `lifeTime`           | Duration the particle remains active (seconds)   |

### Tips

- You can use negative values in hOrbitPeriod to reverse spin direction.

- Adjust emissionInterval for more or fewer particles.

- Use multiple systems with different orbits for layered effects.