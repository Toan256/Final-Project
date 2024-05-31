# SQL3105
## Industry Groups
select*from industry_groups limit 5

| id | industry_group                                                         | 
| -: | ---------------------------------------------------------------------: | 
| 1  | "Consumer Durables, Household and Personal Products"                   | 
| 2  | "Food, Beverage & Tobacco"                                             | 
| 3  | "Forest and Paper Products - Forestry, Timber, Pulp and Paper, Rubber" | 
| 4  | "Mining - Iron, Aluminum, Other Metals"                                | 
| 5  | "Pharmaceuticals, Biotechnology & Life Sciences"                       | 

## Companies
select*from companies limit 5

| id | company_name                  | 
| -: | ----------------------------: | 
| 1  | "Autodesk, Inc."              | 
| 2  | "Casio Computer Co., Ltd."    | 
| 3  | "Cisco Systems, Inc."         | 
| 4  | "CNX Coal Resources, LP"      | 
| 5  | "Coca-Cola Enterprises, Inc." | 

## Countries
select*from countries limit 5

| id | country_name | 
| -: | -----------: | 
| 1  | Australia    | 
| 2  | Belgium      | 
| 3  | Brazil       | 
| 4  | Canada       | 
| 5  | Chile        | 

## Product Emissions
select*from product_emissions limit 5

| id           | company_id | country_id | industry_group_id | year | product_name                                                    | weight_kg | carbon_footprint_pcf | upstream_percent_total_pcf | operations_percent_total_pcf | downstream_percent_total_pcf | 
| -----------: | ---------: | ---------: | ----------------: | ---: | --------------------------------------------------------------: | --------: | -------------------: | -------------------------: | ---------------------------: | ---------------------------: | 
| 10056-1-2014 | 82         | 28         | 2                 | 2014 | Frosted Flakes(R) Cereal                                        | 0.7485    | 2                    | 57.50                      | 30.00                        | 12.50                        | 
| 10056-1-2015 | 82         | 28         | 15                | 2015 | "Frosted Flakes, 23 oz, produced in Lancaster, PA (one carton)" | 0.7485    | 2                    | 57.50                      | 30.00                        | 12.50                        | 
| 10222-1-2013 | 83         | 28         | 8                 | 2013 | Office Chair                                                    | 20.68     | 73                   | 80.63                      | 17.36                        | 2.01                         | 
| 10261-1-2017 | 14         | 16         | 25                | 2017 | Multifunction Printers                                          | 110       | 1488                 | 30.65                      | 5.51                         | 63.84                        | 
| 10261-2-2017 | 14         | 16         | 25                | 2017 | Multifunction Printers                                          | 110       | 1818                 | 25.08                      | 4.51                         | 70.41                        | 

## Combining 4 tables
select*from product_emissions 
left join industry_groups on product_emissions.industry_group_id = industry_groups.id
left join companies on product_emissions.company_id = companies.id
left join countries on product_emissions.country_id = countries.id

| id | company_id | country_id | industry_group_id | year | product_name                                                    | weight_kg | carbon_footprint_pcf | upstream_percent_total_pcf | operations_percent_total_pcf | downstream_percent_total_pcf | industry_group                  | company_name           | country_name | 
| -: | ---------: | ---------: | ----------------: | ---: | --------------------------------------------------------------: | --------: | -------------------: | -------------------------: | ---------------------------: | ---------------------------: | ------------------------------: | ---------------------: | -----------: | 
| 28 | 82         | 28         | 2                 | 2014 | Frosted Flakes(R) Cereal                                        | 0.7485    | 2                    | 57.50                      | 30.00                        | 12.50                        | "Food, Beverage & Tobacco"      | Kellogg Company        | USA          | 
| 28 | 82         | 28         | 15                | 2015 | "Frosted Flakes, 23 oz, produced in Lancaster, PA (one carton)" | 0.7485    | 2                    | 57.50                      | 30.00                        | 12.50                        | Food & Beverage Processing      | Kellogg Company        | USA          | 
| 28 | 83         | 28         | 8                 | 2013 | Office Chair                                                    | 20.68     | 73                   | 80.63                      | 17.36                        | 2.01                         | Capital Goods                   | KNOLL INC              | USA          | 
| 16 | 14         | 16         | 25                | 2017 | Multifunction Printers                                          | 110       | 1488                 | 30.65                      | 5.51                         | 63.84                        | Technology Hardware & Equipment | "Konica Minolta, Inc." | Japan        | 
| 16 | 14         | 16         | 25                | 2017 | Multifunction Printers                                          | 110       | 1818                 | 25.08                      | 4.51                         | 70.41                        | Technology Hardware & Equipment | "Konica Minolta, Inc." | Japan        | 

## Top 5 products with most emission during this period
select 
	product_emissions.product_name as Product,
	industry_groups.industry_group as industry,
	sum(product_emissions.carbon_footprint_pcf) as emission
from product_emissions 
left join industry_groups on product_emissions.industry_group_id = industry_groups.id
left join companies on product_emissions.company_id = companies.id
left join countries on product_emissions.country_id = countries.id
group by product_emissions.product_name
order by sum(product_emissions.carbon_footprint_pcf) desc
limit 5

| Product                      | industry                           | emission | 
| ---------------------------: | ---------------------------------: | -------: | 
| Wind Turbine G128 5 Megawats | Electrical Equipment and Machinery | 3718044  | 
| Wind Turbine G132 5 Megawats | Electrical Equipment and Machinery | 3276187  | 
| Wind Turbine G114 2 Megawats | Electrical Equipment and Machinery | 1532608  | 
| Wind Turbine G90 2 Megawats  | Electrical Equipment and Machinery | 1251625  | 
| TCDE                         | Materials                          | 198150   | 

## Top 5 industries with most emission during this period
select distinct
	industry_groups.industry_group as industry,
	sum(product_emissions.carbon_footprint_pcf) as emission
from product_emissions 
left join industry_groups on product_emissions.industry_group_id = industry_groups.id
left join companies on product_emissions.company_id = companies.id
left join countries on product_emissions.country_id = countries.id
group by industry_groups.industry_group
order by sum(product_emissions.carbon_footprint_pcf) desc
limit 5

| industry                           | emission | 
| ---------------------------------: | -------: | 
| Electrical Equipment and Machinery | 9801558  | 
| Automobiles & Components           | 2582264  | 
| Materials                          | 577595   | 
| Technology Hardware & Equipment    | 363776   | 
| Capital Goods                      | 258712   | 

## Top 5 companies with most emission during this period
select 
	companies.company_name as company,
	industry_groups.industry_group as industry,
	sum(product_emissions.carbon_footprint_pcf) as emission
from product_emissions 
left join industry_groups on product_emissions.industry_group_id = industry_groups.id
left join companies on product_emissions.company_id = companies.id
left join countries on product_emissions.country_id = countries.id
group by companies.company_name
order by sum(product_emissions.carbon_footprint_pcf) desc
limit 5

| company                                 | industry                           | emission | 
| --------------------------------------: | ---------------------------------: | -------: | 
| "Gamesa Corporación Tecnológica, S.A."  | Electrical Equipment and Machinery | 9778464  | 
| Daimler AG                              | Automobiles & Components           | 1594300  | 
| Volkswagen AG                           | Automobiles & Components           | 655960   | 
| "Mitsubishi Gas Chemical Company, Inc." | Materials                          | 212016   | 
| "Hino Motors, Ltd."                     | Automobiles & Components           | 191687   | 

## Top 10 countries with most emission during this period
select 
	countries.country_name as country,
	sum(product_emissions.carbon_footprint_pcf) as emission
from product_emissions 
left join industry_groups on product_emissions.industry_group_id = industry_groups.id
left join companies on product_emissions.company_id = companies.id
left join countries on product_emissions.country_id = countries.id
group by countries.country_name
order by sum(product_emissions.carbon_footprint_pcf) desc
limit 10

| country     | emission | 
| ----------: | -------: | 
| Spain       | 9786130  | 
| Germany     | 2251225  | 
| Japan       | 653237   | 
| USA         | 518381   | 
| South Korea | 186965   | 
| Brazil      | 169337   | 
| Luxembourg  | 167007   | 
| Netherlands | 70417    | 
| Taiwan      | 62875    | 
| India       | 24574    | 

## Trend over years
select
	product_emissions.year,
	sum(product_emissions.carbon_footprint_pcf) as emission
	from product_emissions 
left join industry_groups on product_emissions.industry_group_id = industry_groups.id
left join companies on product_emissions.company_id = companies.id
left join countries on product_emissions.country_id = countries.id
group by product_emissions.year

| year | emission | 
| ---: | -------: | 
| 2013 | 503857   | 
| 2014 | 624226   | 
| 2015 | 10840415 | 
| 2016 | 1640182  | 
| 2017 | 340271   | 
