class DSU{
    public:
    vector<int> size,parent;
    DSU(int n){
        size.resize(n+1,0);
        parent.resize(n+1);
        for(int i=0;i<=n;i++){
            parent[i]=i;
        }
    }
    int findUpar(int i){
        if(parent[i]==i)return i;
        return parent[i]=findUpar(parent[i]);

    }
    void unionbysize(int i,int j){
        if(findUpar(i)==findUpar(j))return ;
        if(size[findUpar(i)]>size[findUpar(j)]){
          
            size[findUpar(i)]+=size[findUpar(j)];
              parent[findUpar(j)]=findUpar(i);

        }else{

            size[findUpar(j)]+=size[findUpar(i)];
             parent[findUpar(i)]=findUpar(j);
        }
    }
};

time complexity of the findupar is alpha (v) which is inverse ackerman function which grows slower than even log, so basically  it's contant for all the applications