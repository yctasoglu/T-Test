# T-Test
Essentially, a t-test allows us to compare the average values of the two data sets and determine if they came from the same population.

# What is t-score?

The t score is a ratio between the difference between two groups and the difference within the groups. The larger the t score, the more similarity there is between groups. The smaller the t score, the more difference there is between groups. 

    A large t-score tells you that the groups are similar.
    A small t-score tells you that the groups are different.
 
	# Example of T-Test

	data1 = [95,100,105,110,115,120] #1st Population

	data2 = [95,96,97,98,99,100,105,106] #2nd population

# compare samples

	stat, p = ttest_ind(data1, data2)
	print('Statistics=%.4f, p=%.4f' % (stat, p))
	
	alpha = 0.050
	
	if p >= alpha:
		print('Same distributions (fail to reject H0)')
	else:
		print('Different distributions (reject H0)')
    
	The interpretation of the statistic finds that the sample means are different, with a significance of at least 5%.
# Output
	Statistics=2.1851, p=0.0494
	Different distributions (reject H0)
