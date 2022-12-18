A quick recap on properties of Fourier series which will be extended to Fourier transforms. ^102bad

#### Fourier Series Basic Fact 1
useful identity: $e^{ikx}=\cos{kx}+i\sin{kx}$
Every continuous function $f(x)$ defined on $\mathbb{R}^1$ and periodic of period $2\pi$ has a Fourier series written
$$f(x)\sim \sum\limits_{k=-\infty}^{\infty}a_k e^{ikx}$$
where
$$a_k = \frac{1}{2\pi}\int_{-\pi}^{\pi}f(x)e^{-ikx}\;dx$$
### Parseval's Identity
$$
\sum\limits_{-\infty}^{\infty}|a_k|^2 = \frac{1}{2}\int_{-\pi}^{\pi}|f(x)|^2\;dx
$$