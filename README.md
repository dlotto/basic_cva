# basic_cva
Building a basic credit valuation adjustment (CVA) calculator.

Following the notebook from Matthias Groncki's blog: [HERE](https://ipythonquant.wordpress.com/2015/04/13/cva-calculation-with-quantlib-and-python/)
* His GitHub: [HERE](https://github.com/mgroncki/IPythonScripts/blob/master/CVA_calculation_I.ipynb)

Following The xVA Challenge 3rd Edition by Jon Gregory
* His spreadsheet are found on his website: [HERE](https://cvacentral.com/books/credit-value-adjustment/spreadsheets/)

## Calculating Expected Exposure
Pricing CVA will involve expected exposure (EE). This is the average of all positive exposure values. Note that only positive values give rise to exposures and other values have a zero contribution (although they contribute in terms of their probability.)

### For a Normal Distribution
$V = \mu + \sigma * Z$
where Z is a standard normal variable.

The definition of exposure is:
$E = max(V, 0) = max(\mu + \sigma * Z, 0)$

**Therefore, expected exposure is:**
EE = mu x T(mu/sigma) + mu x G(mu/sigma)
where,
T = the cumulative normal distribution function
G = normal distribution function

Following Bhuvnesh Khurana on the finrgb.com: [HERE](https://www.finrgb.com/category/swatches/)
* Very detailed and useful videos. Highly recommend.
