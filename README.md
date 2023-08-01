# ShuffleAPI
### This program shuffles and checks for central limit theorem for entries as defined by the user.

###### request method: POST
###### request url: http://100072.pythonanywhere.com/api?api_ke=your_api_key

The parameters that need to be passed by the user from the fronted test screen:
* "Deck Size" <number of entries that are to be shuffled>
* "Test Number" <number of times that you want the deck to be shuffled>
* "Error Size" <This size of the error to be included in shuffled data estimation>


##calling the API using remote Server
    
##### pthon example
```python
import json
import requests

url = "http://100072.pythonanywhere.com/api"

params = {
    "deck": 200, #user defined value can be change but should be >=100
    "error": 1.67, #value can change but should be a floating number
    "test_num": 7, #this is the number of times the data given is shuffled
    "deck_items": '1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66,67,68,69,70,71,72,73,74,75,76,77,78,79,80,81,82,83,84,85,86,87,88,89,90,91,92,93,94,95,96,97,98,99,100' #items to be shuffled
}

get_response = requests.post(url, params)

print(get_response.text)
```
    
##### curl example
 ```
    curl --location 'http://100072.pythonanywhere.com/api' \
    --form 'deck="200"' \
    --form 'error="1.67"' \
    --form 'test_num="7"' \
    --form 'deck_items="\"1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60\""'
  ```
    

### output
1. Means DataFrame
2. Series Dataframe
3. Number of Iterations for optimum series
4. graph data
