# Data Mining Class Work I
## Pooria Assarehha 

### Regression

$$
y = \beta_0 + \beta_1 x + \epsilon_i
$$

$$J = \sum_i^n e_i^2 = \sum_i^n (y_i - \beta_0 - \beta_1 x_i )^2 $$


$$\frac{\partial J}{\partial \beta_0} = \sum_i^n -2(y_i-\beta_0 -\beta_1 x_i) = 0 \quad \Rightarrow \quad \sum_i^n y_i - n \beta_0 - \beta_1 \sum_i^n x_i = 0$$

$$ \Rightarrow \quad \sum_i^n y_i - n \beta_0 - \beta_1 n \bar{x} = 0 \Rightarrow \hat{\beta_0} = \bar{y} - \beta_1 \bar{x}$$

$$\frac{\partial J}{\partial \beta_1} = \sum_i^n -2x_i(y_i-\beta_0 -\beta_1 x_i) = 0 \quad \Rightarrow \quad \sum_i^n x_i y_i - n\bar{x} \beta_0 - \beta_1 \sum_i^n x_i^2 = 0$$


$$\Rightarrow \quad \sum_i^n x_i y_i - n\bar{x} (\bar{y} - \beta_1 \bar{x}) - \beta_1 \sum_i^n x_i^2 = 0 \quad \Rightarrow \quad \sum_i^n x_i y_i - n\bar{x}\bar{y} + n\beta_1 \bar{x}^2 - \beta_1 \sum_i^n x_i^2 = 0$$

$$\Rightarrow \quad \beta_1 ( \sum_i^n x_i^2 - n \bar{x}^2 ) = \sum_i^n x_i y_i - n\bar{x}\bar{y} \quad \Rightarrow \quad  \hat{\beta_1} = \frac{\sum_i^n x_i y_i - \sum_i^n \bar{x}\bar{y}}{\sum_i^n x_i^2 - n \bar{x}^2 } = \frac{\sum_i^n \left(  x_i y_i - \bar{x}\bar{y} \right)}{\sum_i^n x_i^2 - n \bar{x}^2 } $$

$$\Rightarrow \quad \hat{\beta_1} = \frac{\sum_i^n \left(  x_i y_i - \bar{x}\bar{y} \right) + n\bar{x}\bar{y} - n\bar{x}\bar{y}}{\sum_i^n x_i^2 - n \bar{x}^2  - n\bar{x}^2 + n\bar{x}^2 } = \frac{\sum_i^n \left(  x_i y_i - \bar{x}\bar{y} \right) + \sum_i^n y_i \bar{x} - \sum_i^n x_i \bar{y}}{\sum_i^n x_i^2 - 2\bar{x}\sum_i^n x_i  + \sum_i^n\bar{x}^2}$$

$$ = \frac{\sum_i^n \left(  x_i y_i - \bar{x}\bar{y}  + y_i \bar{x} - x_i \bar{y} \right) }{\sum_i^n \left( x_i^2 -2\bar{x}^2 + \bar{x} \right) } = \frac{\sum_i^n \left( x_i - \bar{x} \right)\left( y_i - \bar{y} \right) }{\sum_i^n \left(x_i -\bar{x}\right)^2 } $$

$$
\hat{\beta_1} = \frac{S_{xy}}{S_{xx}} \quad , \quad \hat{\beta_0} = \bar{y} - \hat{\beta_1} \bar{x}
$$
