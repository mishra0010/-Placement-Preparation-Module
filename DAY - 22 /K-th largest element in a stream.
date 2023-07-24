class KthLargest {
public:
priority_queue<int,vector<int>,greater<int>> pq;
int x;
    KthLargest(int k, vector<int>& nums) {
        x = k;
        for(auto &i: nums){
            pq.push(i);
            if(pq.size()>k){
                pq.pop();
            }
        }
    }
    
    int add(int val) {
        pq.push(val);
        if(pq.size()>x){
            pq.pop();
        }
        return pq.top();
    }
};
