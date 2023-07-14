int Solution::solve(vector<int> &A, int B) {
    unordered_map<int,int> mp;
    int ct=0;
    int xorr=0;
    for(int i=0;i<A.size();i++){
        xorr^=A[i];
        if(xorr==B){
            ct++;
        }
        if(mp.find(xorr^B)!=mp.end()){
            ct+=mp[xorr^B];
        }
        mp[xorr]++;
    }
    return ct;
}
