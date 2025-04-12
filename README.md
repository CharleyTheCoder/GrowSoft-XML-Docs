# GrowSoft-XML-Docs

## Particle Systems

Particle systems in Growtopia's custom `ItemRenderer` XMLs define animated visual effects like sparkles, orbits, and glows. Each system contains an `<Emitter>` and a `<Particle>` section.

### Basic Structure

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