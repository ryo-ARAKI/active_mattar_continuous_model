# active_mattar_continuous_model

Implement continuous model describing highly concentrated active matter first proposed in [H. H. Wensink et al. PNAS 2012](https://doi.org/10.1073/pnas.1202032109).

## Continuous model for highly concentrated active matter

The model consists of fourth-order PDE

$$
\frac{\partial \bm{v}}{\partial t} + \lambda_0 \bm{v} \cdot \bm{\nabla} \bm{v} = - \bm{\nabla} p + \lambda_1 \bm{\nabla} \bm{v}^2 - (\alpha + \beta |\bm{v}|^2) \bm{v} - \Gamma_0 \Delta \bm{v} - \Gamma_2 \Delta^2 \bm{v}
$$

and incompressible condition

$$
\bm{\nabla} \cdot \bm{v} = 0
$$

where $\lambda_0, \lambda_1, \Gamma_0$ and $\Gamma_2$ are parameters defining characteristics of the system.

This model can be interpreted as a generalization of incompressible Navier-Stokes equation for passive fluid or Toner-Tu model describing so-called Vicsek model in continuous manner.

## Algorithm

Above equations are numerically solved in a periodic box with Fourier spectral method.

## References

- [Henricus H. Wensink, Jörn Dunkel, Sebastian Heidenreich, Knut Drescher, Raymond E. Goldstein, Hartmut Löwen, and Julia M. Yeomans, Meso-scale turbulence in living fluids, Proc. Natl. Acad. Sci. USA 109 (36) 14308-14313, (2012)](https://doi.org/10.1073/pnas.1202032109)
  - The model is first proposed in this article. Basic assumptions and derivations are addressed in its [supplemental material](https://www.pnas.org/content/suppl/2012/08/17/1202032109.DCSupplemental).
- [Jörn Dunkel, Sebastian Heidenreich, Markus Bär and Raymond E Goldstein, Minimal continuum theories of structure formation in dense active fluids, New J. Phys. 15 045016, (2013)](https://doi.org/10.1088/1367-2630%2F15%2F4%2F045016)
  - Description of model equation is given in section 3.
