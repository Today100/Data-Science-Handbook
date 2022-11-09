# Excercise #1: Photo Tag Analysis

As the input, suppose you have the following list of dictionaries, where each dictionary represents a photo. The task is to group photos with intersecting tags, saving the results to a dictionary called *photo_groups*.

```Python
l = [
 {
  "name": "photo1.jpg",
  "tags": {'coffee', 'breakfast', 'drink', 'table', 'tableware', 'cup', 'food'}
 },
 {
  "name": "photo2.jpg",
  "tags": {'food', 'dish', 'meat', 'meal', 'tableware', 'dinner', 'vegetable'}
 },
 {
  "name": "photo3.jpg",
  "tags": {'city', 'skyline', 'cityscape', 'skyscraper', 'architecture', 'building', 'travel'}
 },
 {
  "name": "photo4.jpg",
  "tags": {'drink', 'juice', 'glass', 'meal', 'fruit', 'food', 'grapes'}
 }
]
```

## Hints:
<details>
  <summary><h3>Iteration</h3></summary>
  To coomplish the task, you'll need to iterate over all possible pairs of photos presented in the list.
  <details>
    <summary>Code</summary>

```Python

for i in range(1, len(l)):
    for j in range(i+1, len(l)+1):
      print(f"Intersection photo {i} with photo {j}")
      # Implement intersection here, saving results to photo_groups
    
```

  </details>
</details>

----------
<details> 
  <summary><h2> Answer for the above dictionary:<h2></summary>

```Python
{
  "tableware_food" : ["photo1.jpg", "photo2.jpg"],
  "drink_food" : ["photo1.jpg", "photo4.jpg"],
  "meal_food" : ["photo2.jpg", "photo4.jpg"]
}
```
</details>


