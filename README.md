# Definir la función
f <- function(x) {
  cos(2 * (x + 0.5 * pi))
}

# Crear valores de x
x_vals <- seq(-2*pi, 2*pi, by = 0.01)

# Crear valores de y
y_vals <- f(x_vals)

# Crear el gráfico
df <- data.frame(x = x_vals, y = y_vals)
ggplot(df, aes(x = x, y = y)) +
  geom_line() +
  labs(x = "x", y = "f(x)", title = "Gráfica de f(x) = cos[2(x+1/2π)]")
