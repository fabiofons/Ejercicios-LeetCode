# Ejercicio LeetCode (Jewels and Stones)

    const numJewelsInStones = function(J, S) {
         let frec = {};
         for (let i = 0; i < J.length; i++) {
           frec[J[i]] = 0;
         }
         for(let i = 0; i < S.length; i++){
           if(frec.hasOwnProperty(S[i])){
              frec[S[i]] += 1;
           }
         }
         let sum = 0;
         for(let jewel in frec){
            sum += frec[jewel];
         }
         return sum;
    };

**Complejidad temporal:O(n+m)**
**Complejidad espacial:O(n)**

# Ejercicio LeetCode (isAnagram)
    const isAnagram = function(s, t) {
        if(s.length != t.length){
          return false;
        }
    
        let obs = {};
        for(let i = 0; i < s.length; i++){
          if(obs.hasOwnProperty(s[i])){
            obs[s[i]] += 1;
          }else{
            obs[s[i]] = 1;
          }
        }
    
        let obt = {};
        for(let i = 0;i < t.length; i++){
          if(obt.hasOwnProperty(t[i])){
            obt[t[i]] += 1;
          }else {
            obt[t[i]] = 1;
          }
        }
    
        for(var letra in obs){
          if(obs[letra] != obt[letra]){
            return false;
         }
        }
        return true;
    };

**Complejidad Temporal:O(n)**
**Complejidad Espacial:O(n)**

# Ejercicio LeetCode (Two-Sum)
    const twoSum = function(nums, target) {
      const obj = {};
      for(var i = 0; i < nums.length; i++){
        const complement = target-nums[i]; 
    
        if(complement in obj){        
          return [obj[complement],i]
        }
    
        obj[nums[i]]=i;
      }  
    };

**Complejidad Temporal:O(n)**
**Complejidad Espacial:O(n)**

