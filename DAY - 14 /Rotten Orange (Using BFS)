class Solution {
public:
    int orangesRotting(vector<vector<int>>& grid) {
        int i,j,a=grid.size(),b=grid[0].size();
        int x = 0;
        queue<vector<int>> q;
        vector<int> v;
        for(i = 0; i < a; i++){
            for(j = 0; j < b; j++){
                if(grid[i][j]==2){
                    q.push({i,j});
                    grid[i][j] = 0;
                }
                x += (grid[i][j]==1);
            }
        }
        if(x==0)return 0;
        int ans = -1,n;
        while(!q.empty()){
            ans++;
            n = q.size();
            while(n--){v = q.front();
            q.pop();
            if(v[0]+1<a&&grid[v[0]+1][v[1]]==1){
                q.push({v[0]+1,v[1]});
                x--;
                grid[v[0]+1][v[1]]=0;
            }
            if(v[1]+1<b&&grid[v[0]][v[1]+1]==1){
                q.push({v[0],v[1]+1});
                x--;
                grid[v[0]][v[1]+1]=0;
            }
            if(v[0]-1>=0&&grid[v[0]-1][v[1]]==1){
                q.push({v[0]-1,v[1]});
                x--;
                grid[v[0]-1][v[1]]=0;
            }
            if(v[1]-1>=0&&grid[v[0]][v[1]-1]==1){
                q.push({v[0],v[1]-1});
                x--;
                grid[v[0]][v[1]-1]=0;
            }}
        }
        return (x==0)?ans:-1;;
    }
};
