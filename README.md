# BH-raytracing
 

# Review

## Kerr metric
The metric for a black hole with mass $`M`$ and angular momentum $`J`$ in Boyer-Lindquist coordiantes ($`t,r,\theta,\phi`$) is
```math
\mathrm{d}{s^2} = -\left(1 - \frac{r_\text{s}r}{\Sigma}\right)\,\mathrm{d}{t^2} + \frac{\Sigma}{\Delta}\,\mathrm{d}{r^2} + \Sigma\,\mathrm{d}{\theta^2} + \left(r^2+a^2+\frac{r_\text{s}ra^2}{\Sigma}\sin^2{\theta}\right)\sin^2{\theta}\,\mathrm{d}{\phi^2} - \frac{2r_\text{s}ra\sin^2{\theta}}{\Sigma}\,\mathrm{d}{t}\mathrm{d}{\phi} \,,
```
where
$$ r_\text{s} = 2G_\text{N}M \,, \qquad a = \frac{J}{M} \,, \qquad \Sigma = r^2+a^2\cos^2{\theta} \qquad\text{and}\qquad \Delta = r^2-r_\text{s}r+a^2 \,. $$
The inner and outer surfaces of the ergosphere and inner and outer (event) horizons are located at
$$r_\text{E}^\pm = \frac{r_\text{s}}{2}\pm\sqrt{\left(\frac{r_\text{s}}{2}\right)^2 - a^2\cos^2{\theta}} \,, \qquad r_\text{H}^\pm = \frac{r_\text{s}}{2}\pm\sqrt{\left(\frac{r_\text{s}}{2}\right)^2 - a^2} \,.$$
From this we find the extremality bound, $\frac{|a|}{G_\text{N}M} = \frac{|J|}{G_\text{N}M^2} \leq 1$.

It will be useful to work in units where $G_\text{N}M = 1$, so that $r_\text{s}=2$ and $a\in[-1,1]$.

## Review of conserved quantities and null geodesics
There are two 'obvious' conserved quantities associated to the Killing vectors $\partial_t$ and $\partial_\phi$, which are the energy $E=-p_t$ and angular momentum $L_z=-p_\phi$. There is a third conserved quantity, the Carter constant $Q=p_\theta^2 - \cos^2{\theta}\left(a^2E^2 - L_z^2\csc^2{\theta}\right)$, which is associated to a Killing tensor. These three constants, along with $p_\mu p^\mu = 0$, are enough to determine a geodesic uniquely.

With affine parameter $\lambda$ (so that $\frac{\mathrm{d}{x^\mu}}{\mathrm{d}{\lambda}} = p^\mu$), trajectories are found by solving
\begin{align}
    \Sigma \frac{\mathrm{d}{r}}{\mathrm{d}{\lambda}} &= \pm\sqrt{R(r)} & R(r) &= P(r)^2 - \Delta\left[(aE-L_z)^2 + Q\right]\\
    \Sigma \frac{\mathrm{d}{\theta}}{\mathrm{d}{\lambda}} &= \pm\sqrt{\Theta(\theta)} & \Theta(\theta) &= Q +\cos^2{\theta}\left(a^2E^2 - L_z^2\csc^2{\theta}\right)\\
    \Sigma \frac{\mathrm{d}{\phi}}{\mathrm{d}{\lambda}} &= -\left(aE-L_z\csc^2{\theta}\right) + \frac{a}{\Delta}P(r) & P(r) &= E\left(r^2+a^2\right) - aL_z\\
    \Sigma \frac{\mathrm{d}{t}}{\mathrm{d}{\lambda}} &= -a\left(aE\sin^2{\theta} - L_z\right) + \frac{r^2+a^2}{\Delta}P(r)
\end{align}
