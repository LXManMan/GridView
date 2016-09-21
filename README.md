# GridView
封装网格view，一行代码，两个代理方法即可实现
 self.gridView =[[GridView alloc]initWithFrame:CGRectMake(0, 0, KScreenW, 200) showGridTitleArray:self.showGridTitleArray showImageGridArray:self.showImageGridArray showGridIDArray:self.showGridIDArray];
    self.gridView.backgroundColor = [UIColor whiteColor];
    self.gridView.gridViewDelegate = self;
    [self.myScrollview addSubview:_gridView];
    [self.gridView updateNewFrame];
}
-(void)updateHeight:(CGFloat)height
{
    self.gridView.height = height;
    self.myScrollview.contentSize = CGSizeMake(KScreenW, height);
}
-(void)clickGridView:(GridButton *)item
{
    NSLog(@"%@",item.gridTitle);
}
