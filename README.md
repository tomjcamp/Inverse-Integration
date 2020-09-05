# Inverse-Integration
Exploring Methods in Quadrature Relating to Inverse Functions


Traditional quadrature methods approximate the integral for smooth functions on a given interval. These methods have defined rate at which their errors approach 0, known as their "order". 

For non-smooth functions, however, these methods tend to break down a bit. For rough functions, the order of the quadrature method can be calculated, but it will definitely be slower. 

We propose here a method which attempts to remedy this issue for special cases. If the function whose integral we wish to approximate over a given interval is invertable on that interval, it may be beneficial to approximate the integral of the functions inverse over that interval instead. This method works theoretically due to results from the Inverse Function Theorem, which states that as $|f'(x)|$ goes to infinity, $|f^{-1}'(f(x))|$ goes to 0, thus "smoothing" the curve whose integral we must approximate. Also, from C.A. Laisant in 1905, we have a method of calculating the integral of a function by the integral of its inverse. 

For the purposes of this program, we call the inverse as the collection of points $(f(x),x)$. This has a few advantages. First, it prevents us from having to explicitly derive the inverse of $f$ directly. Second, we do not have to resample this function over the interval $(f(x_1),f(x_N))$. Finally, if we have a uniform sampling of x on the interval, we have fewer samples of $f^{-1}$ when it is relatively flat, and more samples when it displays a greater slope. This, we eventually hope to prove, increases the accuracy of our quadrature considerably.
