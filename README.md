# md-data-table
A material Data Table component

The structure should be like this
```
<md-data-table sort-data="vm.sortData" filter-data="vm.filterData">
    <md-table-header>
        <md-header-buttons>
            <md-button>ADD</md-button>
            <md-button>UPDATE</md-button>
        </md-header-buttons>
        <md-table-header-row>
            <md-table-column sort-property="id">Identifier</md-table-column>
            <md-table-column sort-property="name">Name</md-table-column>
        </md-table-header-row>
    </md-table-header>
    <md-table-row ng-repeat="item in vm.page.content">
        <md-table-cell>{{ item.id }}</md-table-cell>
        <md-table-cell>{{ item.name }}</md-table-cell>
        <md-table-cell>
            <md-table-editor confirm="vm.commentItem(item)">
                <md-input-container>
                    <input type="text" ng-model="item.comment" />
                </md-input-container>
            </md-table-editor>
        </md-table-cell>
    </md-table-row>
    <md-table-footer count="vm.page.count" 
                     page-size="vm.page.size" 
                     current-page="vm.page.index"
                     page-options="[10, 20, 50, 100]"></md-table-footer>
</md-data-table>
```

# License
MIT

# Author
sergiofilhow@gmail.com