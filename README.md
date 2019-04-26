# Simply-Simulated-Anealing

Initial temperature T, when T=ti iteration times L , time attenuation rate eta, initial answer x0
While t > MinT
  for l=1:L
    value_old = f(x_old)
    find a new value nearly x_old randomly, x_new = x_old + (random() - 0.5)
    compare value_new = f(x_new) and value_old
    if value_new is closer to the best answer than value_old
      x_old = x_new
    else
      accept x_new in possibility (exp(-(value_new - value_old)/k* t)> random())
  t = t * eta
