// The API isBadVersion is defined for you.
// bool isBadVersion(int version);

class Solution {
public: 
    int firstBadVersion(int n) {
        //Descartamos que el primer producto sea el primer error
        if (isBadVersion(1)) return 1;
        
        int left = 1, right = n;
        
        //Aplicamos binary search 
        while(left <= right) {
            int mid = left + (right-left) / 2;
            //Para saber si es el primer erro debemos verificar que el anterior sea correcto
            if(isBadVersion(mid) && !isBadVersion(mid - 1))
                return mid;
            
            else if(isBadVersion(mid)) right = mid - 1;
            
            else left = mid + 1;
        }
        
        
        return 0;
    }
};
