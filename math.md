# Least Squares Algorithm Formulas

## Prediction Formula
$$
y_i \approx \beta_0 + \sum_{j=1}^m \beta_j \times x_j^i
$$

Extending the independent variables:
$$
\vec{x}_i^{\prime} = [1, x_1^i, x_2^i, \ldots, x_m^i]
$$
Then the prediction becomes a dot product:
$$
y_i \approx \sum_{j=0}^m \beta_j \times x_j^i = \vec{\beta} \cdot \vec{x}_i^{\prime}
$$

## Loss Function
The sum of mean squared loss:
$$
\vec{\beta} = \arg\min_{\vec{\beta}} L\left(D, \vec{\beta}\right) = \arg\min_{\vec{\beta}} \sum_{i=1}^n \left( \vec{\beta} \cdot \vec{x}_i - y_i \right)^2
$$

## Matrix Form of Loss Function
$$
L\left(D, \vec{\beta}\right) = \left\| X \vec{\beta} - Y \right\|^2
$$
Expanding the matrix form:
$$
\begin{align}
L\left(D, \vec{\beta}\right) &= \left(X \vec{\beta} - Y\right)^\top \left(X \vec{\beta} - Y\right) \
&= Y^\top Y - Y^\top X \vec{\beta} - \vec{\beta}^\top X^\top Y + \vec{\beta}^\top X^\top X \vec{\beta}
\end{align}
$$

## Gradient of Loss Function
Using denominator layout convention:
$$
\frac{\partial L\left(D, \vec{\beta}\right)}{\partial \vec{\beta}} = -2 X^\top Y + 2 X^\top X \vec{\beta}
$$

