

function mergeSort(arr) {

  if (arr.length <= 1) return arr

  var {lhs, rhs} = splitArr(arr)

  return mergeArr(mergeSort(lhs), mergeSort(rhs) )


}

function splitArr(arr) {

  if (arr.length === 0) return {lhs: [], rhs: []}; 
  if (arr.length === 1) return {lhs: arr, rhs: []};

  var middle = Math.floor(arr.length/2);

  return {lhs: arr.slice(0, middle), rhs: arr.slice(middle)}
}

function mergeArr(lhs, rhs) {

  let resualt = [];
  let lIndex = 0, rIndex = 0;


  while(true){

    if(lhs[lIndex] < rhs[rIndex]){
      resualt.push(lhs[lIndex]);
      lIndex++;
    }else {
      resualt.push(rhs[rIndex]);
      rIndex++;
    }
    if(lIndex == lhs.length || rIndex == rhs.length) break;
  }

  if(lIndex < lhs.length) return resualt.concat(lhs.slice(lIndex));
  if(rIndex < rhs.length) return resualt.concat(rhs.slice(rIndex));

  return resualt
}
