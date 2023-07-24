vector<int> Solution::dNums(vector<int> &A, int B) {

    unordered_map<int,int>mp;

    vector<int>ans;

    int j=0;

    int i=0;

    while(i!=B){

        mp[A[i]]++;

        i++;

    }

    ans.push_back(mp.size());

    for(int i=B;i<A.size();i++){

        mp[A[i]]++;

        mp[A[j]]--;

        if(mp[A[j]]==0) mp.erase(A[j]);

        j++;

        ans.push_back(mp.size());

    }

    return ans;

}
