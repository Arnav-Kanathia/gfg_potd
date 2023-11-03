class Solution{
public:
	// Function to check if the
	// Pythagorean triplet exists or not
	int findroot(int n){
	    int low = 1;
	    int high = n;
	    
	    while(low < high - 1){
	        int mid = low + (high - low) / 2;
	        
	        if(mid * mid > n)
	            high = mid;
	        else
	            low = mid;
	    }
	    
	    return low;
	}
	
	bool checkTriplet(int arr[], int n) {
	    int MAX = *max_element(arr, arr + n);
	    
	    vector<int> f(MAX + 1, 0);
	    
	    for(int i = 0; i < n; i++)
	        ++f[arr[i]];
	        
	    for(int i = 1; i < MAX + 1; i++){
	        for(int j = 1; j < MAX + 1; j++){
	            int sq = i * i + j * j;
	            int k = findroot(sq);
	            
	            if(k > MAX or k * k != sq)
	                continue;
	            
	            --f[i];
	            --f[j];
	            --f[k];
	            
	            if(f[i] >= 0 and f[j] >= 0 and f[k] >= 0){
	                return 1;
	            }
	            
	            ++f[i];
	            ++f[j];
	            ++f[k];
	        }
	    }
	    
	    return 0;
	}
};
