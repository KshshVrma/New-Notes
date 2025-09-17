---
doc_type: hypothesis-highlights
url: 'https://chatgpt.com/c/679112ec-4074-800e-9324-9f5a6bac19ca'
---

# ChatGPT

## Metadata
- Author: [chatgpt.com]()
- Title: ChatGPT
- Reference: https://chatgpt.com/c/679112ec-4074-800e-9324-9f5a6bac19ca
- Category: #article

## Page Notes
## Highlights
- #include <iostream> #include <vector> #include <algorithm> bool compareByFirst(const std::pair<int, int>& a, const std::pair<int, int>& b) { return a.first < b.first; // Ascending order based on the first element }
- int main() { std::vector<std::pair<int, int>> vec = {{3, 2}, {1, 5}, {2, 4}}; std::sort(vec.begin(), vec.end(), compareByFirst); for (const auto& p : vec) { std::cout << "(" << p.first << ", " << p.second << ") "; } return 0; } 

#include <algorithm> bool compareBySecond(const std::pair<int, int>& a, const std::pair<int, int>& b) { return a.second < b.second; // Ascending order based on the second element } int main() { std::vector<std::pair<int, int>> vec = {{3, 2}, {1, 5}, {2, 4}}; std::sort(vec.begin(), vec.end(), compareBySecond); for (const auto& p : vec) { std::cout << "(" << p.first << ", " << p.second << ") "; } return 0; } 







 static bool cmp(pair<pair<int,int>,int>&a, pair<pair<int,int>,int>&b){
      return a.second>b.second;
  }
    vector<int> JobSequencing(vector<int> &id, vector<int> &deadline,
                              vector<int> &profit) {
                                  int maxi=*max_element(deadline.begin(),deadline.end()); 
                                  
        // code here
        vector<int>ans;
        int count=0;
        int sum=0;
        vector<pair<pair<int,int>,int>>vec;
        for(int i=0;i<id.size();i++){
            vec.push_back({{id[i],deadline[i]},profit[i]});
        }
        
        vector<int>jobs(maxi,-1);
        sort(vec.begin(),vec.end(), cmp);
        
        for(int i=0;i<vec.size();i++){
            int ded=vec[i].first.second;
            int pro=vec[i].second;
            
            int j=ded-1;
            while (j>=0){
                if(jobs[j]==-1){
                    jobs[j]=1;
                    sum+=pro;
                    count++;
                    break;
                }
                j--;
                
            }
            
            
        }
       ans.push_back(count);
       ans.push_back(sum);
        
        return ans;
    }

