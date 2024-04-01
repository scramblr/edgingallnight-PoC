# Edge0day [no CVE cuz we ridin dirtyyyy]
# Score: 9/11
# Microsoft Edge Browser Chained Vuln RCE w/Application Guard Bypass.
#
# Pr1v8 d0 n0T D15TR1bu73
# Sh0u75 t0 b1ack0wl for the original 0day
#

## Root cause
We chain multiple URI handler bugs together and stuff some zero width-non-joiners (to throw off MS "Application Guard") into the mix in order to pop calc on ur moms box. 
TL;DR: The URI handler `calculator:` launches `calc.exe` via `ShellExecute` (lol i mean, are u even serious at this point??) and Windows stupidly does not stop this insecure action. MS refused to pay bug bounty so we go public!

## PoC

Open up Microsoft Edge, create "New Application Guard Window" and then open the included `./poc/poc.html` - click the link and it will pop calc! Micro$0ft suuuuxxxxx


