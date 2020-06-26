ng-important-resources
=======

## PrimeNG - Table
  - [Dynamically update table without rerendering the page.](https://www.freakyjolly.com/angular-material-table-operations-using-dialog/#.XvXB888zbDc)
 ```JS
 addRowData(row_obj){
    var d = new Date();
    this.dataSource.push({
      id:d.getTime(),
      name:row_obj.name
    });
    this.table.renderRows();
    
  }
  updateRowData(row_obj){
    this.dataSource = this.dataSource.filter((value,key)=>{
      if(value.id == row_obj.id){
        value.name = row_obj.name;
      }
      return true;
    });
  }
  deleteRowData(row_obj){
    this.dataSource = this.dataSource.filter((value,key)=>{
      return value.id != row_obj.id;
    });
  }
 ```
  
  
  
## Date time formatting
  - [Moment Library](https://momentjs.com/)
