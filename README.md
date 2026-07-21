## Project Overview

This project implements a simplified Fourier-optics phase-mask optimization simulation using the Gerchberg-Saxton algorithm. The goal is to optimize a phase-only mask so that the simulated far-field intensity pattern approximates a desired 2D target.

The project was inspired by Prof. Yang Zhao's group work on uniform 2D target generation using inverse-designed metasurfaces.

## Research Motivation

This project was inspired by recent work on uniform 2D target generation using inverse-designed metasurfaces. Since I am still early in my undergraduate coursework, I developed a simplified Fourier-optics version of the problem.

Instead of modeling real metasurface unit cells, material properties, or fabrication constraints, this project uses a phase-only mask and scalar Fourier propagation. The goal is to understand the basic inverse-design workflow: starting from a desired output intensity pattern, optimize a phase pattern that produces it in the far field.

I tested circle, square, and ring targets, then compared the generated results using error, efficiency, and uniformity-related metrics.

## Limitations

This is not a full electromagnetic metasurface simulation. It does not model real nanostructure geometry, material dispersion, fabrication constraints, near-field effects, or experimental noise.

The project uses a simplified phase-only Fourier-optics model. This helped me understand the computational idea behind inverse design, but further work would require learning physical metasurface design, electromagnetic simulation tools, and fabrication-aware constraints.

## What I Learned

- A target intensity pattern can be represented as a 2D NumPy array.
- A phase mask can be optimized even though it does not visually resemble the target.
- Fourier propagation maps the phase mask to a far-field intensity pattern.
- The Gerchberg-Saxton loop improves the result by alternating between the input plane and far-field plane.
- Efficiency and uniformity are important metrics for evaluating beam-shaping quality.
- Phase quantization gives a simple way to test fabrication-related limitations.
- This simplified model is only a starting point before physical metasurface design.

## Questions For Future Work

1. How is a continuous phase mask converted into real metasurface unit-cell geometry?
2. What simulation tools are commonly used for physical metasurface design?
3. How do fabrication constraints affect the final optical output?
4. How does Gaussian beam illumination change the optimization problem?
5. How do adjoint optimization methods compare with Gerchberg-Saxton?
