# What income to I need to ask for to get my desired income?

## One Tax Bracket

$$ AskedIncome = \frac{DesiredIncome}{1-TaxRate} $$

## Multiple Tax Brackets

$$ AskedIncome = \frac{DesiredIncome-BottomOfClosestIncomeBracket}{1-ClosestTaxRate} + \sum_i^N \frac{(Spread_i)}{(1-TaxRate_i)} $$

$Spread_i  =$  Diff between top and bottom of $i_{th}$ tax bracket

## Example

I want to make $160K a year.  My top tax rate is 24%

If I was just considering one tax bracket, my equation would be $\frac{160000}{1-.24}$
