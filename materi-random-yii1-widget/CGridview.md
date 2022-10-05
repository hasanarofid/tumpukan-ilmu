Contoh Kodingannya
======
```markdown
$this->widget('zii.widgets.grid.CGridView', array(
    'id'=>'user-grid',
    'dataProvider'=>$model->search(),
    'columns'=>array(
        array(
            'name'=>'username',
            'value'=>'$data->username',
        ),
        array(
            'name'=>'image',
            'type'=>'raw', // to encode html string
            'value'=>'$data->image',
        ), 
        array(
            'name'=>'createdon',
            'value'=>'date("Y-m-d",strtotime($data->createdon))',
            // or'value'=>'$data["createdon"]==""?"Not Set":date("Y-m-d",strtotime($data["createdon"]))',
        ), 
        array(
            'name'=>'isactive',
            'value'=>'$data["isactive"]==1?"Active":"Inactive"',
        ),
        array(
            'class'=>'CButtonColumn',
        ),
    ),
))

```

Hasilnya
======
Here's our logo (hover to see the title text):

Inline-style: 
![alt text](https://github.com/RSDS-SOETOMO/tumpukan-ilmu/blob/master/tutorial-markdown/hela.jpg "Logo Title Text 1")

Reference-style: 
![alt text][logo]

[logo]: ../tutorial-markdown/hela.jpg "Logo Title Text 2"
