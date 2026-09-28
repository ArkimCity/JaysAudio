# Imported measurement sources

The files below were retrieved on 2026-09-29. They are kept in their source
format wherever possible; JaysAudio's parser reads the first two numeric
columns as frequency and level.

## Bluetooth comparison set

[Open QCY N70, EarFun Air Pro 4, Nothing Ear (3a), and SOUNDPEATS H3 together](https://arkimcity.github.io/JaysAudio/?share=QCY_N70_ANC,Earfun_Air_Pro_4_ANC,Nothing_Ear_%283a%29,SOUNDPEATS_H3)

The preset uses the ANC-on ReganCipher variants for QCY and EarFun. The H3
source does not identify an ANC state. SoundGuys publishes only an averaged
frequency response for the Nothing Ear (3a).

### QCY N70

- Source: [ReganCipher Squiglink](https://regancipher.squig.link/)
- Product reference: [ReganCipher QCY N70 review](https://regancipher.com/reviews/2025/10/qcy-n70-review/)
- Imported variants: ANC off/default and ANC on/default, left and right
- Source files: `QCY N70[ ANC] [L|R].txt`
- Transformation: numerical data and headers retained; line endings were
  normalized to LF and trailing whitespace was removed

### EarFun Air Pro 4

- Source: [ReganCipher Squiglink](https://regancipher.squig.link/)
- Imported variants: ANC off/default and ANC on/default, left and right
- Source files: `Earfun Air Pro 4[ ANC] [L|R].txt`
- Transformation: numerical data and headers retained; line endings were
  normalized to LF and trailing whitespace was removed

### SOUNDPEATS H3

- Source: [Avishai Squiglink](https://avishai.squig.link/)
- Imported variant: source-default tuning, left and right
- Source files: `SOUNDPEATS H3 [L|R].txt`
- Transformation: numerical data and headers retained; line endings were
  normalized to LF and trailing whitespace was removed
- Selection note: ReganCipher's public H3 left/right files were byte-identical
  at retrieval time, so the independently measured Avishai pair was used
  instead of presenting a duplicated curve as two channels.

### Nothing Ear (3a)

- Product identity: [Nothing Ear (3a)](https://intl.nothing.tech/products/ear-3a)
- Measurement source: [SoundGuys lab data](https://www.soundguys.com/product/nothing-ear-3a/)
- Methodology: [SoundGuys headphone testing](https://www.soundguys.com/how-we-test/)
- Imported variant: public left/right average frequency response
- Source file: `Nothing Ear (3a) L.txt`
- Transformation: the 241 published chart points were copied without smoothing
  or resampling. The single averaged response occupies the loader's `L` slot;
  it is not a claim that SoundGuys published an individual left channel.

## Comparability limits

These curves do not all come from one measurement rig. ReganCipher and Avishai
publish REW measurements from their own setups, while SoundGuys uses a
Brüel & Kjær 5128 head simulator and publishes an averaged, normalized curve.
Normalization in JaysAudio aligns levels but cannot remove fixture, insertion,
tip, smoothing, or unit-to-unit differences. Use the combined view for broad
tonal comparison, not for fine cross-source conclusions—especially above the
ear-canal resonance region.
