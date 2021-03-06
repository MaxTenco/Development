# Components

1. [Select](#select)
2. [$resource](#resource)

---

## Select

* **Initialize the select**
  ``` Javascript
  $scope.nameSelect = {selected: '', options: [], visibility: false};
  ```

* **Populate the select:**
  
  ``` Javascript
  /**
  * Populates the select of Name
  */
  function populateNameSelect()
  {
    var options = ['A', 'B', 'C'];
    $scope.nameSelect.options = options;
  }
  ```
* **Method on change item:**
``` Javascript
  /**
  * Event when the Name Select changes the selected value
  */
  function onNameChange()
  {
         
  }
  ```

* **View**
  * With only value
  ``` HTML
   <select ng-options="item for item in nameSelect.options"
           ng-model="nameSelect.selected"
           ng-change="onNameChange()">
    </select>
  ```
  * Selected the empty value option
  ``` HTML
    <option style="display:none" value="">Select...</option>
  ```

* **ng-options** 


| For array data sources | Exaple |
|------------------------| ------ |
| label for value in array |
| select as label for value in array | **ng-options**:`"option.value as option.key for option in arrayName"`</br> **output**:`<option value="value">key</option>` |
| label group by group for value in array                                                                |
| label disable when disable for value in array                                                          |
| label group by group for value in array track by trackexpr                                             |
| label disable when disable for value in array track by trackexpr                                       |
| label for value in array | orderBy:orderexpr track by trackexpr (for including a filter with track by) |


|For object data sources| Example |
| --------------------- | ------- |
|label for (key , value) in object|  |
|select **as** label **for** (key , value) **in** object | `key as value for (key, value) in object` </br> `<option value="key">value</option>` |
|label group by group for (key, value) in object|
|label disable when disable for (key, value) in object|
|select as label group by group for (key, value) in object|
|select as label disable when disable for (key, value) in object|

---

## $resource
| Method | URL | Code |
|--------| --- | ---- |
| POST | user/{id} | `{url: 'user/:id', method: 'POST', params: {id: 'id'}}` |

