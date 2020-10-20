# Longest-subarray-with-distinct-elements
Given an array of elements, return the length of the longest subarray where all its elements are distinct.  For example, given the array [5, 1, 3, 5, 2, 3, 4, 1], return 5 as the longest subarray of distinct elements is [5, 2, 3, 4, 1].

#include<bits/stdc++.h>
using namespace std;
//function to add largest subarray with no duplicates
int largestsubarray(int a[], int n)
{
	//stores array of index elements
	unorderedmap<int,int>index;
	int ans=0;
	for(int i=0,j=0;i<n;i++)
	{
		//update j based on previous occurence of a[i]
		j=max(index[a[i],j);
		//update ans to store maximum length of subarray
		ans=max(ans,i-j+1);
		//store the index of current occurence of a[i]
		index[a[i]]=i+1;
	}
	//return final ans
	return ans;
}
//driver code
int32_t main()
{
	int arr={1,2,3,4,1,3,5,6};
	int n=sizeof(arr)/sizeof(arr[0]);
	cout<<largestsubarray(arr,n);
}
	

