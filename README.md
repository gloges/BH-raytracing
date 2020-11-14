# BH-raytracing




## Kerr metric

The metric for a black hole with mass _M_ and angular momentum _J_ in Boyer-Lindquist coordinates (_t,r,θ,φ_) is

<img src="https://render.githubusercontent.com/render/math?math=\large\qquad\mathrm{d}s^2 = -\left(1-\frac{r_sr}{\Sigma}\right)\,\mathrm{d}t^2 %2B \frac{\Sigma}{\Delta}\,\mathrm{d}r^2 %2B \Sigma\,\mathrm{d}\theta^2 %2B \left(r^2 %2B a^2 %2B \frac{r_sra^2}{\Sigma}\sin^2{\theta}\right)\,\sin^2{\theta}\,\mathrm{d}\phi^2 - \frac{2r_sra\sin^2{\theta}}{\Sigma}\,\mathrm{d}t\,\mathrm{d}\phi \,,">

where

<img src="https://render.githubusercontent.com/render/math?math=\large\qquad r_s = 2G_N M \,, \qquad\qquad a = \frac{J}{M} \,, \qquad\qquad \Sigma = r^2 %2B a^2\cos^2{\theta}  \,, \qquad\qquad \Delta = r^2 - r_sr %2B a^2 \,.">

For convenience choose units where <img src="https://render.githubusercontent.com/render/math?math=G_NM = 1">, so that <img src="https://render.githubusercontent.com/render/math?math=r_s=2"> and <img src="https://render.githubusercontent.com/render/math?math=a\in[-1,1]">. With this choice the inner and outer horizons are located at <img src="https://render.githubusercontent.com/render/math?math=r_\pm = 1 \pm \sqrt{1-a^2}">.


## Conserved quantities and null geodesics

There are two "obvious" conserved quantities associated to the Killing vectors <img src="https://render.githubusercontent.com/render/math?math=\partial_t"> and <img src="https://render.githubusercontent.com/render/math?math=\partial_\phi">, which are the energy <img src="https://render.githubusercontent.com/render/math?math=E=-p_t"> and angular momentum <img src="https://render.githubusercontent.com/render/math?math=L_z=-p_\phi">. There is also a third conserved quantity, the Carter constant:

<img src="https://render.githubusercontent.com/render/math?math=\large\qquad Q = p_\theta^2 - \cos^2{\theta}\left(a^2E^2-L_z^2\csc^2{\theta}\right) \,,">

which is associated to a Killing tensor. These three constants of motion, along with <img src="https://render.githubusercontent.com/render/math?math=p_\mu p^\mu = 0">, are enough to determine a null geodesic uniquely. With affine parameter _λ_ (so that <img src="https://render.githubusercontent.com/render/math?math=\frac{\mathrm{d}x^\mu}{\mathrm{d}\lambda} = p^\mu">), trajectories are found by solving the following equations of motion,

<img src="https://render.githubusercontent.com/render/math?math=\large\qquad \Sigma\frac{\mathrm{d}t}{\mathrm{d}\lambda} = -a\left(aE\sin^2{\theta} - L_z\right) %2B \frac{r^2 %2B a^2}{\Delta}P(r) \,, \qquad \Sigma\frac{\mathrm{d}r}{\mathrm{d}\lambda} = \pm\sqrt{R(r)} \,, \qquad \Sigma\frac{\mathrm{d}\theta}{\mathrm{d}\lambda} = \pm\sqrt{\Theta(\theta)} \,, \qquad \Sigma\frac{\mathrm{d}\phi}{\mathrm{d}\lambda} = - \left(aE - L_z\csc^2{\theta}\right) %2B \frac{a}{\Delta} P(r) \,,">

where the potentials are

<img src="https://render.githubusercontent.com/render/math?math=\large\qquad P(r) = E(r^2 %2B a^2) - aL_z \,, \qquad R(r) = P(r)^2 - \Delta\left(Q %2B (aE-L_z)^2\right) \,, \qquad \Theta(\theta) = Q %2B \cos^2{\theta}\left(a^2E^2 - L_z^2\csc^2{\theta}\right) \,.">

Since the above coordinates are singular at the outer horizon, it is useful to shift to coordinates which are smooth at the outer horizon when integrating the geodesic equations:

<img src="https://render.githubusercontent.com/render/math?math=\large\qquad \mathrm{d}v = \mathrm{d}t %2B \frac{r^2 %2B a^2}{\Delta}\,\mathrm{d}r \,, \qquad \mathrm{d}\varphi = \mathrm{d}\phi %2B \frac{a}{\Delta}\,\mathrm{d}r \,.">




