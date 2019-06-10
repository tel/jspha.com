---
title: 'Growing a music theory'
date: Mon, 30 Nov -0001 00:00:00 +0000
draft: true
tags: []
---

People often laud music theory as being _beautiful_ and _mathematical_. I've often wondered what they were smoking.

Sure, there are a fair number of appealing symmetries, but to my eye there are a much greater number of idiosyncrasies and facts that you just had to memorize. For every nice rule like "inverted intervals add to 9" and the circle of fifths you also get clunkers like E being the same as Fb.

At one level you just have to chalk it up to hundreds of years of western musical culture and cruft. At another level it's deeply unsatisfying. Music comes from physics! It should have absolutely beautiful theory.

More than that, there should be a theory which unifies music from practices beyond just the western heritage. It's deeply unsatisfying to say _Oh, Indian ragas use notes "kind of in between" the notes in the Western scale_. There should be a theory which covers all of this!

So, let me share it with you.

_Note before I begin: I'm mostly speaking to people with familiarity and interest in mathematics here as opposed to music theorists, composers, musicologists._

A beautiful theory of harmony
-----------------------------

Here's the punchline: pick a tonal center and then iteratively build more pitches by multiplying by small powers of small primes: the more complex the relative prime decomposition the more dissonant the harmony.

Which is dense and inscrutable and so totally insufficient as any sort of explanation. It's also dense and inscrutable and _just enough_ to re-derive the whole endeavor. That's the right feeling and the rest of this article will be unpacking that idea.

As we dig in, you are possibly going to have to forget everything you know about music theory for a minute. The punchline there is that for practical purposes around instrument construction, band management, and notation people in the Western tradition "broke" the simple theory above. We'll recover all that stuff, but not immediately.

To start, we need to instead look at what harmony and consonance mean from a psychophysical perspective.

Tuning for beats
----------------

Any instrumentalist is familiar with the "beats" that occur when you're turning an instrument. Two similar sounds played together at very slightly different pitches will create a slow "pulsation". Many people learn to tune their instruments by eliminating the beating sound.

\[Insert audio sample\]

Mathematically, we can see the beating effect as the sum-product rule from trigonometry

$latex \\sin{\\left((\\alpha - \\epsilon) t\\right)} + \\sin{\\left((\\alpha + \\epsilon) t\\right)} = 2 \\sin{(\\alpha t)} \\cos{(\\frac{\\epsilon}{2} t)}$

where $latex \\alpha$ is the average pitch and $latex \\epsilon$ is the how far out of tune each instrument is. The $latex \\cos$ component on the right side is the beating effect and as $latex \\epsilon$ shrinks the beats get slower and slower. Eventually they just become a ["phasing" effect](https://www.youtube.com/watch?v=Bzp5LdSvo1o) as the two pitches are considered in tune.

A sense of dissonance
---------------------

When beats are particularly slow we get something that's psycho-acoustically interesting and pleasing. On the other side of the spectrum, as the pitches drift further and further apart the "beating" sensation disappears as we begin to clearly distinguish the two pitches.

What's awful is right in the middle when two pitches are close, but not too close, together. This is the sound of poor tuning, of mistaken harmonies, of just general awfulness. This is the sound of dissonance.

In order to build a pleasing system of consonant, harmonic pitches we simply have to avoid or control dissonance. This is almost sufficient to explain the "small powers of small primes" rule, but we need to explore one more sonic phenomenon first.

Fourier series and periodic signals
-----------------------------------

It's almost too fundamental to say, but when talking about harmonies we tend to be interested in sounds which are, well, _harmonic_ as opposed to _inharmonic_ sounds. More than just wordplay, though, these words speak to the "harmonic structure" of a sound.

Generally, "harmonic sounds" are those we recognize as having a pitch while "inharmonic sounds" are those without any strong pitch. You could compare the sound of a violin string being bowed to the sound of a snare drum being hit. Or a human voice versus white noise.

Mathematically, harmonicity has to do with how the energy of the sound lays out in spectral space.

References
----------

*   [Gary Garrett's animations](http://www.garygarrett.me/?page_id=87)
*   [W. A. Mathieu](https://amzn.to/2Hybrxe) _[Harmonic Experience](https://amzn.to/2Hybrxe)_
*   [Wikipedia "Just Intonation"](https://en.wikipedia.org/wiki/Just_intonation)