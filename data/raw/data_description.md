# Data Description

This file contains the description of the variables in both the clients and the prices datasets.

## client_data.csv

- `id`: client company identifier
- `channel_sales` : code of the sales channel
- `cons_12m` : electricity consumption of the past 12 months
- `cons_gas_12m` : gas consumption of the past 12 months
- `cons_last_month` : electricity consumption of the last month
- `date_activ` : date of activation of the contract
- `date_end` : registered date of the end of the contract
- `date_modif_prod` : date of the last modification of the product
- `date_renewal` : date of the next contract renewal
- `forecast_cons_12m` : forecasted electricity consumption for next 12 months
- `forecast_cons_year` : forecasted electricity consumption for the next calendar year
- `forecast_discount_energy`: forecasted value of current discount
- `forecast_meter_rent_12m` : forecasted bill of meter rental for the next 2 months
- `forecast_price_energy_off_peak` : forecasted energy price for 1st period (off peak)
- `forecast_price_energy_peak` : forecasted energy price for 2nd period (peak)
- `forecast_price_pow_off_peak` : forecasted power price for 1st period (off peak)
- `has_gas` : indicated if client is also a gas client
- `imp_cons` : current paid consumption
- `margin_gross_pow_ele` : gross margin on power subscription
- `margin_net_pow_ele` : net margin on power subscription
- `nb_prod_act` : number of active products and services
- `net_margin` : total net margin
- `num_years_antig` : antiquity of the client (in number of years)
- `origin_up` : code of the electricity campaign the customer first subscribed to
- `pow_max` : subscribed power
- `churn` : has the client churned over the next 3 months

## price_data.csv

- `id` : client company identifier
- `price_date` : reference date
- `price_off_peak_var` : price of energy for the 1st period (off peak)
- `price_peak_var` : price of energy for the 2nd period (peak)
- `price_mid_peak_var` : price of energy for the 3rd period (mid peak)
- `price_off_peak_fix` : price of power for the 1st period (off peak)
- `price_peak_fix` : price of power for the 2nd period (peak)
- `price_mid_peak_fix` : price of power for the 3rd period (mid peak)

**Note: some fields are hashed text strings. This preserves the privacy of the original data but the commercial meaning is retained.**
