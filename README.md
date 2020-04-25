# hello-word
bool Company::DeleteBus2(int  number)
{
    int i;
    for(i=0; i<size; i++)
    {
        bus1=bus[i];
        if(bus1->number==number)
        {
            for(int j=i; j<size; j++)
            {
                bus1=bus[j];
                (bus1->number)--;
                bus[j]=bus[j+1];
                if(j==size-1)
                    number=bus1->number ;
            }
            cout<<"该车信息已删除!"<<endl;
            size--;
            return true;
        }
    }
    if(i==size)
    {
        cout<<"未找到该车信息,无法删除!"<<endl;
        return false;
    }
    return false;
}
 
void Company::DeleteBus()     //删除车辆
{
    /*
    Company类的函数，根据用户输入的车辆名称判断车辆信息是否存在，
    若存在，查找并显示所有此名称的车辆，再提示用户根据显示出的车辆信息选择要删车的车辆
    */
    int num;
    cout<<"-->>删除车辆"<<endl;
    show();
    cout<<"请选择要删除的车辆的编号："<<endl;
    cin>>num;
    DeleteBus2(num);
    cout<<"请按任意键继续..."<<endl;
    fflush(stdin);
    getchar();
    Keyboard_entry();
}
