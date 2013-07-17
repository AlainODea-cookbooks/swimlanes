swimlanes Cookbook
==========================
Override node attributes with swimlane attributes if node['swimlane'] is present.

Requirements
------------
swimlanes works with base Chef.

You need to create a `swimlanes` data bag with items for each lane.  Each lane
item should be structured to populate the root of the node attributes hierarchy.

Only those attributes you want to override need be present for this to work.

Attributes
----------
#### swimlanes::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['swimlanes']['swimlane']</tt></td>
    <td>String</td>
    <td>The name of an item in the swimlanes data bag to override node
      attributes from</td>
    <td><tt>Nil</tt></td>
  </tr>
</table>

Usage
-----
#### swimlanes::default
Just include `swimlanes` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[swimlanes]"
  ]
}
```

Contributing
------------
1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write you change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

License and Authors
-------------------
 * Author: Alain O'Dea

Copyright: 2013, Alain O'Dea

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
