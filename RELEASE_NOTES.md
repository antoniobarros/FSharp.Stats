#### 0.1.1 - Thursday, November 7, 2019
Several bugfixes and additions to multiple namespaces. 
The documentation and unit tests have been extended.

* **FSharp.Stats** (core)
    * Additional functionalities:
	  * [Sparse Matrix initialization] (https://github.com/CSBiology/FSharp.Stats/commit/94d2d3030a6c390a2a0947730c5feeea77b937b0) 
	  * [Sparse Matrix multiplication] (https://github.com/CSBiology/FSharp.Stats/commit/0f908c5d0af7efc7919b658d8dc7778cd7369e15) replaced implementation to gain performance
	  * [Sparse Matrix QR decomposition] (https://github.com/CSBiology/FSharp.Stats/commit/b098fe21d49a91ec49159ef015768563fa9887cb)
      * [Spectral matrix norm](https://github.com/CSBiology/FSharp.Stats/commit/7d27b03457b746d054a1fe81f57db66ccdb1b903)
	  * [Generalized weighted pearson correlation] (https://github.com/CSBiology/FSharp.Stats/commit/33b449881a1884371416c34dcdd9335202d2a758)
	  
* **FSharp.Stats.Fitting** 
    * Additional functionalities:
	  * [Crossvalidation kFold] (https://github.com/CSBiology/FSharp.Stats/commit/4ef896b88636fe6161adfe76fbd0daebb5d54bf9)
	  * [RidgeRegression] (https://github.com/CSBiology/FSharp.Stats/commit/7e66392bb126eaeaabe4453f3101648adeb531c4)
	  * [Levenberg Marquardt implementation supporting box constrains] (https://github.com/CSBiology/FSharp.Stats/commit/5c1d95aa062bb14a9947cdffdd53f7d90a0f8e5a)
	  
* **FSharp.Stats.Signal** 
    * Additional functionalities:
	  * [Estimate optimal window width for savitzky golay filters](https://github.com/CSBiology/FSharp.Stats/commit/d1f7a7ef58ce3a82992a912e7c85a8f4b572f347)
	  * [BaselineALS'] (https://github.com/CSBiology/FSharp.Stats/commit/30bfc3fcba531f7c834b708416915296ff4e3363) internal use of sparse matrices to increase performance
		
* **FSharp.Stats.ML** 
	* Additional functionalities:
	  * [Set similarity measures] (https://github.com/CSBiology/FSharp.Stats/commit/fd1ec1e9d135750db63a2589093da5bb89505e94) 
	  * [Energy landscape plot to SA](https://github.com/CSBiology/FSharp.Stats/commit/46daf7f44a3683cd7d16b900ce67ffce70392101)
	  * [GapStatistics] (https://github.com/CSBiology/FSharp.Stats/commit/e02a2dfa5291868e547f2be4813887e6342320c4) assists cluster number optimization


#### 0.1.0 - Wednesday, July 3, 2019
Several bugfixes and additions to multiple namespaces: 

* **FSharp.Stats** (core)
    * Additional functionalities:
      * [Matrix FSI printer](https://github.com/CSBiology/FSharp.Stats/commit/15b12b07278162fe1ddc5b5a2bc9975615c7a388) for increasing convenience when working with matrices
      * Biweight midcorrelation for [sequences](https://github.com/CSBiology/FSharp.Stats/commit/f85c362e121c72fdc501539f401b6bf8e89514a4), [vectors and matrices](https://github.com/CSBiology/FSharp.Stats/commit/84c4369e0b84eda8ac67d43362d93168427ed0f4)
    * Bug fixes:
      * Fix shuffle functions to not shuffle in place (commits [2816d81](https://github.com/CSBiology/FSharp.Stats/commit/2816d81eed86fdf3ceb4a754635cda698f96f3ab) and [475874d](https://github.com/CSBiology/FSharp.Stats/commit/475874d58a1c73d3a7bdcf6f3c49e3179cbf34d0))

* **FSharp.Stats.Fitting**
    * Additional functionalities:
      * [Weighted polynomial least squares fitting](https://github.com/CSBiology/FSharp.Stats/commit/723ae6514947c93e992cba17549646cd8db6beab) to cope with heteroscedacity
      * [Adjusted coefficient of determination](https://github.com/CSBiology/FSharp.Stats/commit/78ffe3d540478c1814eacaff5079a3ff43259fb4) to incorporate the number of required variables
      * [Leave-out-one cross validation](https://github.com/CSBiology/FSharp.Stats/commit/7b81f4198a6b48d948e2f30bef023e1205c1f788)
      * [Exponential fit](https://github.com/CSBiology/FSharp.Stats/commit/6050c6bb67d08bc1c06008601442af4c124b2ca7) model in non-linear regression
      * [Theil-Sen estimator](https://github.com/CSBiology/FSharp.Stats/commit/5c433181e0b7a1529a54bf64ec9fd16447187fdb) for robust linear regression
      * [Weighted pearson correlation](https://github.com/CSBiology/FSharp.Stats/commit/e03123933ee2bc3b3dd2e6da54892f2b9254ee27) to cope with heteroscedacity
      * Calculate derivatives for [polynomial regression](https://github.com/CSBiology/FSharp.Stats/commit/fa78afeedb9cda2563f6c7554588f1439782cfd9)

* **FSharp.Stats.Interpolation**
    * Additional functionalities:
      * [Polynomial interpolation](https://github.com/CSBiology/FSharp.Stats/commit/b8e72d3d22eabcdc1a68aba67a2139b7ea9d44a1)
      * [Cubic spline interpolating](https://github.com/CSBiology/FSharp.Stats/commit/5036d4ed666218ad9cb82a91b7db489e1742d424) with several boundary conditions
      * [Cubic Hermite spline](https://github.com/CSBiology/FSharp.Stats/commit/d9ac98d74904b19fa338dc35c3f1e676f3926b54) with [simple slope estimator](https://github.com/CSBiology/FSharp.Stats/commit/49ee64e5aea6a0dfb8504e0807260b31fd1148ed)
      * [Get monotonicity slopes](https://github.com/CSBiology/FSharp.Stats/commit/8de4caa2a31c5cbd5192597b375911d6a8ce96ec) that if possible fit an monotone interpolating cubic spline
      * Calculate derivatives for [interpolating polynomials](https://github.com/CSBiology/FSharp.Stats/commit/23682c65d8a6088a0cc3a919e2975729eda36687) and [interpolating cubic splines](https://github.com/CSBiology/FSharp.Stats/commit/98a74fe9222b39cfca2c5641879d99b689251aec)

* **FSharp.Stats.Integration**
    * Additional functionality:
      * [TwoPointDifferentiation](https://github.com/CSBiology/FSharp.Stats/commit/7bd502ca0c02de9cb9218ccbb7b1a7468881f6b9#diff-ea4073dc197d0496ca8c047f82974244)

* **FSharp.Stats.Algebra**
    * Additional functionality:
      * Calculation of the [nullpace of a matrix](https://github.com/CSBiology/FSharp.Stats/commit/723ae6514947c93e992cba17549646cd8db6beab) based on SVD

* **FSharp.Stats.Signal**
    * Additional functionalities:
      * [Ricker wavelet](https://github.com/CSBiology/FSharp.Stats/commit/60c6b16710d79bd0e87da8b6e0d1f6d8c33ecde4) for 2D continuous wavelet transform
      * [Marr wavelet](https://github.com/CSBiology/FSharp.Stats/commit/6f77aba16befaf22bb430900a25b5a59e204e0bc) for 3D continuous wavelet transform
      * [Signal padding](https://github.com/CSBiology/FSharp.Stats/commit/a575b7a7cd7260cffd28bb4bc903297e2ba11985)
      * [Continuous wavelet transform](https://github.com/CSBiology/FSharp.Stats/commit/90eb89eba11335c73ee4f6f181b421bf7bfb0029) with [defaultCWT](https://github.com/CSBiology/FSharp.Stats/commit/117e551a9c3d1c9798ce0aa2ff7b3f9027808322) and [discrete CWT](https://github.com/CSBiology/FSharp.Stats/commit/4feda5959b0024c7834e5d82c87cd1411f237d35)

* **FSharp.Stats.MSF**
    * Several improvements for Hermite (Temporal Classification):
      * commit [c0d98de](https://github.com/CSBiology/FSharp.Stats/commit/c0d98de77840a25a76712302dcca383646e52b95)  
        * add extrema calculation of constrained spline
        * add third extrema constraints
        * add various weighting methods
        * add corrected AIC model selection criterion



#### 0.0.14 - Friday, April 12, 2019
* PCA
#### 0.0.13 - Wednesday, December 12, 2018
* Fix pValueAdjust
#### 0.0.12 - Tuesday, December 11, 2018
* Fix median
#### 0.0.11 - Monday, December 10, 2018
* Bump version to 0.0.11
#### 0.0.1 - Tuesday, July 3, 2018
* Initial release
