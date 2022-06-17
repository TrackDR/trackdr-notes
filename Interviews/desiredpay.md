# What income to I need to ask for to get my desired income?

## One Tax Bracket

$$ Ask4Income = \frac{DesiredIncome}{1-TaxRate} $$

## Multiple Tax Brackets

$$ Ask4Income = \frac{DesiredIncome-BottomOfClosestIncomeBracket}{1-ClosestTaxRate} + \sum_i^N \frac{(Spread_i)}{(1-TaxRate_i)} $$

$Spread_i  =$  Diff between top and bottom of $i_{th}$ tax bracket

## Example

I want to make $120K a year.  My top tax rate is 24%

If I was just considering one tax bracket, my equation would be $\frac{120000}{1-.24} = $157894.74$
