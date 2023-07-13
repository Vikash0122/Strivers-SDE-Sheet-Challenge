# Implement Trie

~~~
class Trie {

public:

    struct TrieNode {
        bool isEnd;
        TrieNode *child[26];
    };
    TrieNode* getNode() {
        TrieNode *newNode = new TrieNode();
        newNode->isEnd=false;
        for(int i=0; i<26; i++){
            newNode->child[i]=NULL;
        }
        return newNode;
    }
    TrieNode *root;
    Trie() {
        root=getNode();
    }
    
    void insert(string word) {
        TrieNode *curr=root;
        for(char ch: word){
            int index= ch-'a';
            if(curr->child[index]==NULL){
                curr->child[index] = getNode();
            }
            curr=curr->child[index];
        }
        curr->isEnd=true;
    }

    
    bool search(string word) {
        TrieNode *curr=root;
        for(char ch: word) {
            int index=ch-'a';
            if(curr->child[index]==NULL){
                return false;
            }
            curr=curr->child[index];
        }
        if(curr->isEnd==true) return true;

        return false;
    }
    
    bool startsWith(string prefix) {
        TrieNode *curr=root;
        int count=0;
        for(char ch: prefix) {
            count++;
            int index=ch-'a';
            if(curr->child[index]==NULL){
                return false;
            }
            curr=curr->child[index];
        }
        if(count==prefix.length()) return true;
        return false;
    }
};
~~~
