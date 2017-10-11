# Summary

Business, corporate, and purchasing cards are used just like personal credit and debit cards. However, these cards carry higher interchange rates because they offer employers high value (and costly) features such as enhanced reporting and statements. Many merchants can qualify for lower commercial rates by collecting the more in‑depth Level 2 and Level 3 data with each commercial card transaction.

See [Level 2 and Level 3 Fields](https://github.com/PayFabric/APIs/wiki/Level-2-and-Level-3-Fields) to understand what is level 2 and level 3 fields and how PayFabric support your business to integrate.

PayFabric is helping merchants avoid incautious downgrading by supporting merchants setup default value for some of level 2 and level 3 fields. Navigate through Main > Configuration > L2/3 Fields Default, you will open below screen.

![l23default](https://s3-us-west-1.amazonaws.com/github-screenshot-repository/v2/L23default.png)

# Details

## Gateway Account

L2/3 Fields Default is configured by gateway account profiles. 

## Applying Logic

There're two ways to apply the default fields:

1. **Apply default values only when the developers submit level 2/3 data**. By choosing this option, the default settings apply only if developer send level 2/3 fields proactively. PayFabric is going to fill the missing fields based on your settings.

1. **Apply default values, whether the developer submits level 2/3 data or not**. By choosing this option, the default settings always apply even if developer doesn't send level 2/3 at all.  
