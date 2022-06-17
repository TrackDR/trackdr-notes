# What income to I need to ask for to get my desired income?

## One Tax Bracket

$$ Ask4Income = \frac{DesiredIncome}{1-TaxRate} $$

## Multiple Tax Brackets

$$ Ask4Income = \frac{DesiredIncome-BottomOfClosestIncomeBracket}{1-ClosestTaxRate} + \sum_i^N \frac{(Spread_i)}{(1-TaxRate_i)} $$

$Spread_i  =$  Diff between top and bottom of $i_{th}$ tax bracket

## Example - Single Tax Bracket 24%

I want to make $120K a year.  My tax rate is 24%

If I was just considering one tax bracket, my equation would be $\frac{120000}{1-.24} = 157894.74$

So I need to ask for $157894.74 to get $120K after taxes with a single tax bracket of 24%.

## Example - Multiple Tax Brackets

The US Federal Income Tax uses tax brackets
- 10% for Income Up to $10,275 
- 12% for Income $10,276 to $41,775
- 22% for Income $41,776 to $89,075
- 24% for Income $89,076 to $170,050
