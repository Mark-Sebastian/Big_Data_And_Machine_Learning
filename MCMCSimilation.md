MCMCFunction = function(length = 10, numPaths = 5, SD = 0.05){
	par(mfrow = c(1,1))
	dta1 = rnorm( length, 0, SD)
	dta2 = dta1 + 1
	dta3 = cumprod(dta2) 
	plot(data2, type = "l", col = 0,
	main = "MCMC Simulation"
	lty = 1, ylim=c(-5,5)
	xlim = c(1,length))
	for(i in 0:(numPaths)){
		dta1 = rnorm( length, 0, SD)
		dta2 = dta1 + 1
		dta3 = cumprod(dta2) 
		lines(dta3, col = i, lty = i)
	}
}
MCMCFunction(100,20)
