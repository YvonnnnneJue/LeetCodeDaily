```
/**
 * @param {string} s
 * @return {string}
 */
var replaceSpace = function(s) {
    const arr = [...s];
    let count = 0;

    let oldLen = arr.length;
    for(let i =0;i<oldLen;i++){
        if(arr[i]===' ')
        count++;    
    }

    // let left = arr.length - 1;
    arr.length += count * 2

    for(let left = oldLen - 1,right = arr.length - 1; left >= 0; left--, right--){
        if(arr[left] != ' '){
            arr[right] = arr[left]
        }else{
            arr[right-2] = '%';
            arr[right-1] = '2';
            arr[right] = '0';
            right -= 2;
        }
    }
    
        return arr.join('')
    
};
```