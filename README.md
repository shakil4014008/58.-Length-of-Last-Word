# 58.-Length-of-Last-Word

```C#
   #Solution 1: 
   
       public int LengthOfLastWord(string s) {
        int count =0;
        int i=s.Length-1;
        
        while(i>=0){
            if(s[i] != ' '){
                count++;
            }
            
            if(s[i] == ' ' && count>0){
                return count;
            }
            i--;
        } 
        
        return count;  
    }
    
    
    #Solution 2: 
      public int LengthOfLastWord(string s) {
    
        s = s.Trim();
       
        if(s.Length == 0) return 0;
        
       int index = 0;
        
       for(int i=0; i<s.Length; i++){
           if(Char.IsWhiteSpace(s[i]))
              index = i;            
       } 
      
       int count = 0;
       if(index == 0)
       {
            for(int i=0; i<s.Length; i++){
              count++;
            }
           return count;
       }
       
       string str = s.Substring(index+1); 
       for(int i=0; i<str.Length; i++){
            count++;
       }
       
        return count;
    }
```
