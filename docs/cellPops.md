## Cell populations equations

Fitness is a measure of how well a cell can reproduce and it depends on the vigor $V$ (availability of resources), base rate $f_0$ and the fraction $k$ of cooperation $c$ (how much of the resources the cell gives others).

For healthy cells (h): $V = c = 1$

For cancerous cells (c): $V = 1, c = 0$

For senescent cells (s): $V = 0, c = 1$

For cells that are both senescent and cancerous (b): $V = c =0$

Using new term $\beta_i$ to set removal rates of the different types of cells.

$\frac{dN_i}{dt} = (r_i)N_i + mutations$


where: $r_i = f_i - \beta_i$ and $f_i = f_0 v(1-kc)$

Healthy:

$$\frac{dN_h}{dt} = r_hN_h - \mu_c N_h -  \mu_v N_h$$

$$ N_h(t) = e^{(f_h-\mu_v-\mu_c)t}     $$

Cancerous:

$$ \frac{dN_c}{dt} = r_cN_c + \mu_c N_h -  \mu_v N_c $$

$$ N_c(t) = \frac{\mu_c}{f_c -f_h + \mu_c}(e^{(f_c - \mu_v)t} - e^{(f_h - \mu_v - \mu_c) t}) $$

Senescent:

$$ \frac{dN_s}{dt} = f_sN_s - \mu_c N_s +  \mu_v N_h $$

$$    N_s(t) = \frac{\mu_v}{f_s -f_h + \mu_v}(e^{(f_s - \mu_c)t} - e^{(f_h - \mu_v - \mu_c) t})     $$

Both:

$$ \frac{dN_b}{dt} = f_bN_b + \mu_c N_s +  \mu_v N_c $$

$$  N_b = (\frac{(a+d)}{(b-f_b)} - \frac{a}{(c-f_b)} - \frac{d}{(g-f_b)})e^{k_bt} -\frac{(a+d)}{(b-f_b)}e^{bt} + \frac{a}{(c-f_b)}e^{ct} + \frac{d}{(g-f_b)}e^{gt} $$ 

Where: $ a =  \frac{\mu_c\mu_v}{f_s -f_h + \mu_v}$,

 $b = f_h - \mu_v -\mu_c$,

 $c = f_s - \mu_c$,

 $ d =  \frac{\mu_c\mu_v}{f_c -f_h + \mu_c}$, 

$g = f_c - \mu_v$

