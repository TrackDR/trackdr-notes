# Desired Pay (What is my Actual Income if I ask for a certain income?)

## One Tax Bracket

$$ ActualIncome = \frac{AskedIncome}{1-TaxRate} $$

## Multiple Tax Brackets

$$ ActualIncome = \frac{AskedIncome-BottomOfClosestIncomeBracket}{1-ClosestTaxRate} + \sum_i^N (Spread_i)(TaxRate_i) $$

$Spread_i  =$  Diff between top and bottom of $i_{th}$ tax bracket
