---
layout: defaultpost
title: "Week 11 Hash Table Resizing"
date: 2016-06-27
---

Today's toy problem involved writing the resizing function in a hash table. Hash tables generally resize after reaching a certain capacity, and in this case it was 75%. During the data structures sprint, I rewrote a hash table but not the resizing portion, so this was a first for me. However, I knew the concept of how it worked and remembered the inner structure of a hash table and its insert and remove function. So the resizing function would have similar logic in the index hashing.<br />
It takes a newSize and sets the previous storageLimit to be the newSize, which is usually 2x larger. So if the storageLimit is 4, and the hash table resizes, after resizing the new storageLimit would be 8. A new array is also instantiated, newStorage, to hold the new hash table. Then we iterate over the storage array, and if the index in the storage array exists, iterate over that bucket. If the element in the newStorage at the hashed index does not exist, set it equal to an empty array. We use the hashing function which takes a key and size, and pass in the current bucket's array's key and the storageLimit to return a new index to push into the newStorage array's bucket at the hashed index. At the end, we set the storage equal to the newStorage and the hash table has been resized. The time complexity of a resizing is linear O(n), and it is because of this resizing that makes hash table insertion amortized constant O(1).
<br />

```
function resize(newSize) {
  storageLimit = newSize;
  const newStorage = [];
  storage.forEach(bucket => {
    bucket.forEach(pair => {
      const index = getIndexBelowMaxForKey(pair[0], storageLimit);
      newStorage[index] = newStorage[index] || [];
      newStorage[index].push([pair[0], pair[1]]);
    });
  });
  storage = newStorage;
}
```