# hello-word
We will create a project.
bool Company::FindBusNam1(char *name1)
{
    for(int i=0; i<size; i++)
    {
        bus1=bus[i];
        if(strcmp(bus1->name,name1)==0)
        {
            cout<<"路线名称为"<<bus1->name<<"的公交车的信息为："<<endl;
            cout<<setiosflags(ios::left)<<"          *         "<<setw(8)<<"编号"<<setw(8)<<"名称"<<setw(8)<<"类型"<<setw(8)<<"起点站"<<setw(8)<<"终点站"<<"*"<<endl;
            cout<<setiosflags(ios::left)<<"          *         "<<setw(8)<<bus1->number<<setw(8)<<bus1->name<<setw(8)<<bus1->type<<setw(8)<<bus1->start<<setw(8)<<bus1->terminal<<setw(8)<<"*"<<endl;
            return true;
        }
        if(i==size)
        {
            cout<<"无该车任何信息！"<<endl;
            return false;
        }
        return false;
    }
}
 
void Company::FindBusNam()      //判断车辆信息是否存在，查找车辆
{
    char name11[10];
    cout<<"请输入要查找车辆的名称："<<endl;
    cin>>name11;
    FindBusNam1(name11);
    cout<<"请按任意键继续..."<<endl;
    fflush(stdin);
    getchar();
    Keyboard_entry();
}
