/********headerfile******/
#include<iostream>
#include<string.h>
#include<fstream>
#include<conio.h>
using namespace std;
/****/
const int len=30;
/**classcustomer**/
class customer
{
	private:
		int c_id;
		int c_age;
		char c_name[len];
		int r_charge;
		char c_occ[len]; //occupation
		char room_type[len];
	public:
		int indate,odate;
		int inmonth,omonth;
		int inyear,oyear;
		int food;
		int room;
		int t;
		int otherchar;
		int no_day;
		void add_cus();
		void update_cus();
		void search_cus();
		void show_cus();
		void checkin_cus();
		void checkout_cus();
		void room_detail();
		void gene_bill();
		int retidno();
};
/**classbill**/
class bill:public customer
{
	private:
		int room_charge;
		char cust_name[len];
		char bi;
	public:
		void calculatebill()
		{cin.ignore();
			cout<<"\n\n\n\t\t\t\tEnter Room Type ";
		    cout<<"\n\n\n\n\t\t1) Super Luxury Suit\n\n\t\t2) Luxury Suit\n\n\t\t3) Suit\n\n\n\t\t\tEnter Your Choice: ";
		    cin.get(bi);
		    switch(bi)
		    {case '1':
		    	room_charge=4000; break;
		     case '2':
		     	room_charge=3000; break;
		     case '3':
		     	room_charge=1500;break;
		     default:
		        cout<<"\n\tWrong choice ...";
				cout<<"\n\tERROR: Room is not allocated.";
                cout<<"\n\tBill cannot be created ";
			}cin.ignore();
			cout<<"\n\t\tEnter Bill of Restaurant: ";	
			cin>>food;
			cout<<"\n\t\tEnter Additional Charges(Include charges of spa and gym ): ";
				cin>>otherchar;
			cout<<"\n\t\tEnter No.of Days: ";	cin>>no_day;
			cin.ignore();			
			room=room_charge*no_day;
			t=room+food+otherchar;
        }	
		void display_bill()		
		{	cout<<"\n\n\n\t\t\tBILL";
			cout<<"\n\tDays Stayed for: "<<no_day;
			cout<<"\n\tRoom Charges(per day): "<<room_charge;
			cout<<"\n\tRoom Charges(total ): "<<room;
			cout<<"\n\n\n\n\t\tCustomer Check-In Date : "<<indate<<"/"<<inmonth<<"/"<<inyear;
            cout<<"\n\n\n\n\t\tCustomer Check-Out Date : "<<odate<<"/"<<omonth<<"/"<<oyear;
			cout<<"\n\tRestaurant Bill: "<<food;
			cout<<"\n\tAdditional Charges: "<<otherchar;
			cout<<"\n\n\n\tTotal Bill Amount: \t\t"<<t;
		}
};
/**class employee**/
class employee
{
	private:
		int e_id;
		int e_age;
		char e_name[len];
		char e_title[len];
		int e_salary;
	public:
		void add_emp();
		void show_emp();
		int rettidno();
		void gene_bill();
		int food;
		int house;
		int t;
		int otherchar;
		int no_mon;
};
/*bill employee class*/
class billemp:public employee
{
	private:
		int h_rent;
		char bi;
	public:
		void calculatebille()
		{cin.ignore();
			cout<<"\n\n\n\t\t\t\tEnter House Type ";
		    cout<<"\n\n\n\n\t\t1) Super Luxury \n\n\t\t2) Luxury \n\n\t\t3) Deluxe\n\n\n\t\t\tEnter Your Choice: ";
		    cin.get(bi);
		    switch(bi)
		    {case '1':
		    	 h_rent=4000; break;
		     case '2':
		     	 h_rent=3000; break;
		     case '3':
		     	 h_rent=1500;break;
		     default:
		        cout<<"\n\tWrong choice ...";
				cout<<"\n\tERROR: Room is not allocated.";
                cout<<"\n\tBill cannot be created ";
			}cin.ignore();
			cout<<"\n\n\t\t\t\t\tEnter Bill of Restaurant: ";	
			cin>>food;
			cout<<"\n\n\t\t\t\t\tEnter Additional Charges(Include charges of pick and drop service ): ";
				cin>>otherchar;
			cout<<"\n\n\t\t\t\t\t Enter No.of Months: ";	cin>>no_mon;
			cin.ignore();			
			house=h_rent*no_mon;
			t=house+food+otherchar;
        }	
		void display_bille()		
		{	cout<<"\n\n\n\t\t\tBILL";
			cout<<"\n\n\t\t\t\t\t Months Stayed for: "<<no_mon;
			cout<<"\n\n\t\t\t\t\t House Rent(per month): "<<h_rent;
			cout<<"\n\n\t\t\t\t\t House Rent(total ): "<<house;
			cout<<"\n\n\t\t\t\t\t Restaurant Bill: "<<food;
			cout<<"\n\n\t\t\t\t\t Additional Charges: "<<otherchar;
			cout<<"\n\t\t\t\t\t Total Bill Amount: \t\t"<<t;
		}
};
/*customer & bill func's*/
//gene_bill
void customer::gene_bill()
{ bill b;
b.calculatebill();
b.display_bill(); 
}
//checkin
void customer::checkin_cus()
{
		char ch;
		cout<<"\n\n\n\n\t\t\t\t\t Enter Customer Checkin Date(dd/mm/yy):";
		cin>>indate>>ch>>inmonth>>ch>>inyear;
		room_detail();
    	cin.ignore();
        cout<<"\n\n\n\n\t\t\t\t\t Enter Room Type: ";
		cin.get(room_type,len);
        cin.ignore();
        cout<<"\n\n\n\n\t\t\t\t\t Enter Room Charge: ";
        cin>>r_charge;
}
//add_cus
void customer::add_cus()
{
  cout<<"\n\n\n\n\t\t\t\t\tEnter Customer Id :\t";
  cin>>c_id;
  cout<<"\n\n\n\n\t\t\t\t\tEnter Customer Name :\t";
  cin.ignore();
  cin.get(c_name,len);
  cout<<"\n\n\n\n\t\t\t\t\tEnter Customer Occupation:\t";
  cin.ignore();
  cin.get(c_occ,len);
  cin.ignore();
  cout<<"\n\n\n\n\t\t\t\t\tEnter Customer Age :\t";
  cin>>c_age;
  checkin_cus();
  cout<<"\n\n\n\n\t\t\t\t\"Record Entered Successfuly\"";
}
//dp_cus
void customer::show_cus()
{
    cout<<"\n\n\n\n\t\t\t\t\t Customer Id :\t"<<c_id;
    cout<<"\n\n\n\n\t\t\t\t\t Customer Name :\t"<<c_name;
    cout<<"\n\n\n\n\t\t\t\t\t Customer Occupation:\t"<<c_occ;
    cout<<"\n\n\n\n\t\t\t\t\t Customer Age :\t"<<c_age;
    cout<<"\n\n\n\n\t\t\t\t\t Customer Check-In Date : "<<indate<<"/"<<inmonth<<"/"<<inyear;
    if((odate!=0)&&(omonth!=0)&&(oyear!=0))
    	cout<<"\n\n\n\n\t\t\t\t\t Customer Check-out Date : "<<odate<<"/"<<omonth<<"/"<<oyear;
	cout<<"\n\t\t\t\t\t Room Type: "<<room_type;
    cout<<"\n\n\t\t\t\t Room Charge: "<<r_charge;
}
//cuscheckout
void customer::checkout_cus()
{		char ch;
		cout<<"\n\n\n\n\t\t\t\t\t Enter Customer Id:\t";
		cin>>c_id;
		cin.ignore();
		cout<<"\n\n\n\n\t\t\t\t\t Enter Customer Checkout Date(dd/mm/yy):";
		cin>>odate>>ch>>omonth>>ch>>oyear;
		room_detail();
    	cin.ignore();
        cout<<"\n\n\n\n\t\t\t\t\t Enter Room Type: ";
		cin.get(room_type,len);
        cin.ignore();
        cout<<"\n\n\n\n\t\t\t\t\t Enter Room Charge: ";
        cin>>r_charge;
		/*    if((omonth==2)&&(odate>29))
        {cout<<"\n\n\t\t\tWRONG INPUT";
        cout<<"\n\n\tKindly Re-enter Info\n";
		goto let;
		}
		 if((omonth>12)&&(odate>31))
        {cout<<"\n\n\t\t\tWRONG INPUT";
        cout<<"\n\n\tKindly Re-enter Info\n";
		goto let;
		}
		 if((omonth==4||omonth==6||omonth==9||omonth==11)&&(odate>30))
        {cout<<"\n\n\t\t\tWRONG INPUT";
        cout<<"\n\n\tKindly Re-enter Info\n";
		goto let;
		}
		 if((oyear%4)!=0 &&(omonth==2)&&(odate>28))
        {cout<<"\n\n\t\t\tWRONG INPUT";
        cout<<"\n\n\tKindly Re-enter Info\n";
		goto let;}*/
		
}
//room detail
void customer::room_detail()
{
	 	cout<<"\n\n\n\t\t\t\t Rooms Type ";
		cout<<"	\n\n\n\n\t\t1) Super Luxury Suit Charge=4,000";
		cout<<"	\n\n\n\n\t\t2) Luxury Suit Charge=3,000";
		cout<<"	\n\n\n\n\t\t3) Suit Charge=1,500";
}
//returnid no
int customer::retidno()
{
	return c_id;
}
/*func for employee*/
//bill
void employee::gene_bill()
{ billemp bb;
bb.calculatebille();
bb.display_bille(); 
}
//add
void employee::add_emp()
{
  cout<<"\n\n\n\n\t\tEnter Employee Id :\t";
  cin>>e_id;
  cout<<"\n\n\n\n\t\tEnter Employee Name :\t";
  cin.ignore();
  cin.get(e_name,len);
  cout<<"\n\n\n\n\t\tEnter Employee Title:\t";
  cin.ignore();
  cin.get(e_title,len);
  cin.ignore();
  cout<<"\n\n\n\n\t\tEnter Employee Age :\t";
  cin>>e_age;
  cout<<"\n\n\n\n\t\tEnter Employee Salary :\t";
  cin>>e_salary;
  cout<<"\n\n\n\n\t\t\t\tRecord Entered Successfuly";
}
//show
void employee::show_emp()
{ cout<<"\n\n\n\n\t\t\t\t\t Employee Id :\t"<<e_id;
  cout<<"\n\n\n\n\t\t\t\t\t Employee Name :\t"<<e_name;
  cout<<"\n\n\n\n\t\t\t\t\t Employee Title:\t"<<e_title;
  cout<<"\n\n\n\n\t\t\t\t\t Employee Age :\t"<<e_age;
  cout<<"\n\n\n\n\t\t\t\t\t Employee Salary :\t"<<e_salary;
}
//rettidno em
int employee::rettidno()
{
	return e_id;
}
/*file func declaration for cus*/
void write_cus();	//function to write record in binary file
void display_cus();	//function to display cus details given by user
void modify_cus(int);	//function to modify record of file
void delete_cus(int);	//function to delete record of file
void search_cus(int); //function to search record of file
void out(int);
void billl();
/*file fun declarations for empl*/
void write_emp();	//function to write record in binary file
void display_emp();	//function to display cus details given by user
void modify_emp(int);	//function to modify record of file
void delete_emp(int);	//function to delete record of file
void search_emp(int); //function to search record of file
void bille();
/*file func definition for cus*/
//write
void write_cus()
{	customer cus;
     char ans;
	//cout<<"\n\n\n\n\t\t\tAdd customer record\n";
	ofstream outFile;
	do{
	outFile.open("customer.dat",ios::binary|ios::app);
	cus.add_cus();
	outFile.write((char *) &cus,sizeof(customer));
	outFile.close();
	cout<<"Want To Add Another Record\t"; cin.get(ans);
}while(ans=='Y'||ans=='y');
}
//search
void search_cus()
{   customer cus;
char ans;
	int flag=0,id;
	ifstream inFile;
    do{
	inFile.open("customer.dat",ios::binary|ios::in);
	if(!inFile)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
	cout<<"\n\n\tEnter The id No. : "; cin>>id;
	cout<<"\nCustomer DETAILS\n";
    while(inFile.read((char*)&cus,sizeof(customer)))
	{
		if(cus.retidno()==id)
		{
			cus.show_cus();
			flag=1;
		}
	}
    inFile.close();
	if(flag==0)
		cout<<"\n\nCustomer does not exist";
	cout<<"\n\t\t\t\t\tWant To Search Another Customer(Y/N)\t";
	cin.ignore(ans);
	}while(ans=='Y'||ans=='y');
}
//display
void display_cus()
{	customer cu;
char ans;
int a=0;
	ifstream inFile;
	inFile.open("customer.dat",ios::in);
	if(!inFile)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
//	cout<<"\n\n\t\tEmployee\n\n";
	while(inFile.read((char*)&cu,sizeof(customer)))
	{if (a==0){
		cu.show_cus();
		 cout<<"\n\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
		cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
		cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
		cout<<"\n";
		   getch();
	      a=1;}
	}
	if(a==0)
	cout<<"\n\n\n\n\n\n\n\t\t\tNo Record Found";
	
	inFile.close();
}
//modify
void modify_cus()
{int found=0,id;
	customer cus;
	char ans;
	fstream File;
	do{
    File.open("customer.dat",ios::binary|ios::in|ios::out);
	if(!File)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
	cout<<"Enter customer id: ";cin>>id;
    while(File.read((char *) &cus, sizeof(customer)) && found==0)
	{
		if(cus.retidno()==id)
		{
			cus.show_cus();
			cout<<"\n\nEnter The New Details of Customer"<<endl;
			cus.add_cus();
		int pos;
		long large=sizeof(customer);
		pos=(-1)*large;
			File.seekp(pos,ios::cur);
		    File.write((char *) &cus, sizeof(customer));
		    found=1;
		  }
	}
	File.close();
	if(found==0)
		cout<<"\n\n Record Not Found ";
	cout<<"\n\n\tWant To Modify Another Record(Y/N) ";
	cin.get(ans);
	}while(ans=='Y'||ans=='y');
}
//del
void delete_cus()
{
    customer cus;
    char ans;
    int id;
	ifstream inFile;
	ofstream outFile;
	do{
	inFile.open("customer.dat",ios::binary);
	if(!inFile)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
	cout<<"Enter customer id: ";cin>>id;
	outFile.open("Temp.dat",ios::binary);
	inFile.seekg(0,ios::beg);
	while(inFile.read((char*)&cus,sizeof(customer)))
	{
		if(cus.retidno()!=id)
		{
			outFile.write((char*)&cus,sizeof(customer));
		}
	}
    inFile.close();
	outFile.close();
	remove("customer.dat");
	rename("Temp.dat","customer.dat");
	cout<<"\n\n\tRecord Deleted ..";
	cout<<"\n\n\tWant To Delete Another Record(Y/N) ";
	cin.ignore(ans);	
}while(ans=='Y'||ans=='y');
}
//out
void out(int id)
{
	customer cus;
	int flag=0;
	char ans;
	fstream file;
do{
  file.open("customer.dat",ios::binary|ios::in|ios::out);
	if(!file)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
//	cout<<"\n\n\tEnter The id No. : "; cin>>id;
	cus.checkout_cus();
	cout<<"\n\tCustomer DETAILS\n";
    while(file.read((char*)&cus,sizeof(customer)))
	{
		if(cus.retidno()==id)
		{
			//cus.checkout_cus();
			cus.show_cus();
		
			flag=1;
			file.write((char*)&cus,sizeof(customer));
		}
	}
	file.close();
	if(flag==0)
		cout<<"No search record exist";
	else 
		cout<<"\n\n\nCheckout date added";	
	cout<<"\n\n\tWant To Add Another Checkout Date(Y/N) ";
	cin.ignore(ans);	
}while(ans=='Y'||ans=='y');
}
//bill
void billl()
{
	customer cus;
	char ans;
	ofstream outFile;
do{
	outFile.open("customer.dat",ios::binary|ios::app);
	cus.gene_bill();
	outFile.write((char *) &cus, sizeof(customer));
	outFile.close(); 
	cout<<"\n\n\nBill Created ";
	cout<<"\n\n\tWant To Create Another Bill";
	cin.ignore(ans);	
}while(ans=='Y'||ans=='y');
}
//*func definition for emp*/
//write em
void write_emp()	
{	employee em;
char ans;
//	cout<<"\n\n\n\n\t\t\tAdd Employee Record\n";
	do{
	ofstream outFile;
	outFile.open("employee.dat",ios::binary|ios::app);
	em.add_emp();
	outFile.write((char *) &em, sizeof(employee));
	outFile.close();
	cout<<"\n\n\tWant to Add Another Employee Record(Y/N) ";
	cin.ignore(ans);
}while(ans=='Y'||ans=='y');
}
//dp em
void display_emp()	
{	employee em;
int flag=0;
	ifstream inFile;
	inFile.open("employee.dat",ios::in);
	if(!inFile)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
//	cout<<"\n\n\t\tEmployee\n\n";
	while(inFile.read((char*)&em,sizeof(employee)))
	{if (flag==0)
		em.show_emp();
		 cout<<"\n\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
		cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
		cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
		cout<<"\n";
		   getch();
		   flag=1;		   
	}
	if(flag==0)
	cout<<"\n\n\n\n\n\n\n\t\t\tNo Record Found";
	inFile.close();
}
//searchem
void search_emp(int id)
{   employee em;
	int flag=0;
	char ans;
	ifstream inFile;
    do{
	inFile.open("employee.dat",ios::binary|ios::in);
	if(!inFile)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
	//cout<<"\n\n\tEnter The id No. : "; cin>>id;
	cout<<"\n\tEmployee DETAILS\n";
    while(inFile.read((char*)&em,sizeof(employee)))
	{
		if(em.rettidno()==id)
		{
			em.show_emp();
			flag=1;
		}
	}
    inFile.close();
	if(flag==0)
		cout<<"\n\nCustomer does not exist";
		cout<<"Want to Search another Employee(Y/N)  ";
		cin.ignore(ans);
}while(ans=='Y'||ans=='y');
	
}
//modify emp
void modify_emp(int id)	
{	employee em;
	int found=0;
	fstream File;
	char ans;
	do{
    File.open("employee.dat",ios::binary|ios::in|ios::out);
	if(!File)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
//	cout<<"Enter Employee id: ";cin>>id;
    while(File.read((char *) &em, sizeof(employee)) && found==0)
	{
		if(em.rettidno()==id)
		{
			em.show_emp();
			cout<<"\n\nEnter The New Details of Employee"<<endl;
			em.add_emp();
		int pos;
		long large=sizeof(employee);
		pos=(-1)*large;
			File.seekp(pos,ios::cur);
		    File.write((char *) &em, sizeof(employee));
		    found=1;
		  }
	}
	File.close();
	if(found==0)
		cout<<"\n\n\tRecord Not Found";
		cout<<"Want to Modify Another Record(Y/N)";
		cin.ignore(ans);
}while(ans=='Y'||ans=='y');
}
//delete em
void delete_emp(int id)
{
    employee em;
    char ans;
	ifstream inFile;
	ofstream outFile;
	do{
	inFile.open("employee.dat",ios::binary);
	if(!inFile)
	{
		cout<<"File could not be open !! Press any Key...";
		return;
	}
//	cout<<"Enter Employee id: ";cin>>id;
	outFile.open("Tempp.dat",ios::binary);
	inFile.seekg(0,ios::beg);
	while(inFile.read((char*)&em,sizeof(employee)))
	{
		if(em.rettidno()!=id)
		{
			outFile.write((char*)&em,sizeof(employee));
		}
	}
    inFile.close();
	outFile.close();
	remove("employee.dat");
	rename("Tempp.dat","employee.dat");
	cout<<"\n\n\tRecord Deleted ..";
	cout<<"\n\n\tWant to Delete Another Record(Y/N) ";
	cin.ignore(ans);
}while(ans=='Y'||ans=='y');
}
//bille
void bille()
{
	employee em;
	ofstream outFile;
	char ans;
	do{
	outFile.open("employee.dat",ios::binary|ios::app);
	em.gene_bill();
	outFile.write((char *) &em, sizeof(employee));
	outFile.close(); 
	cout<<"\n\n\nBill Created ";
	cout<<"Want to Create Another Bill(Y/N) ";
	cin.ignore(ans);
	}while(ans=='Y'||ans=='y');	
}
void logo();
void logo()
{cout<<"  HOTEL MANAGEMENT SYSTEM";
cout<<"\n  \xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD";
}
/*main func*/
int main()
{
	char ch;
	int num;
	int id,m=1,n=1;
	char user[len],ch1,ch2,ch3,ch4;
	logo();
	cout<<"\n\n\n\n\n\n\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD";
	cout<<"\t\t" "\t\t\t\t\t\t\tHOTEL MANAGEMENT SYSTEM";
	cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD";
do{
	cout<<"\n\n\n\t\t\t\tHotel MainMenu Login";
	cout<<"\n\t\t\t\t\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4\xC4";
cout<<"\n\n\n\n\n\n\t\t\t\t\t\t\t\tEnter User Name:\t";
cin.get(user,len);
cin.ignore();
cout<<"\n\n\t\t\t\t\t\t\t\tEnter Password:\t";
	ch1=getch();
	printf("*");
	ch2=getch();
	printf("*");
	ch3=getch();
	printf("*");
	printf("*");
	ch4=getch();
	printf("*");
     system("cls");
	if(ch1=='a'&&ch2=='b'&&ch3=='c'&&ch4=='d')

{
		do
	{system("cls");
	
	logo();
		cout<<"\n\n\n\n\n\n\n\t\t\t\t\t\t\t\t\t\tMAIN MENU";
		cout<<"\n\t\t\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n\n";
		cout<<"\n\n\t\t\t\t\t\t\t\t\t01.Administrator";
		cout<<"\n\n\t\t\t\t\t\t\t\t\t02.Search Employee";
		cout<<"\n\n\t\t\t\t\t\t\t\t\t03.Search Customer";
		cout<<"\n\n\t\t\t\t\t\t\t\t\t04.Exit";
		cout<<"\n\n\t\t\t\t\t\t\t\tEnter Your Choice:\t";
		cin>>ch;
		switch(ch)
		{case'1':
		  do{system("cls");
		  logo();
		  cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tAdministrator Login";
		  cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
		  	cout<<"\n\n\t\t\t\t\t\t\t\tEnter Password:\t";
			ch1=getch();
			printf("*");
			ch2=getch();
			printf("*");
			ch3=getch();
			printf("*");
			printf("*");
			ch4=getch();
			printf("*");
		    system("cls");
			if(ch1=='e'&&ch2=='f'&&ch3=='g'&&ch4=='h')
            {do{
		  	system("cls");
		  	logo();
			cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tAdministrator";
			cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
			cout<<"\n\n\t\t\t\t\t\t\t\t\t01. Customer";
			cout<<"\n\n\t\t\t\t\t\t\t\t\t02. Employee";
			cout<<"\n\n\t\t\t\t\t\t\t\t\t03. Exit";
			cout<<"\n\n\t\t\t\t\t\t\t\tEnter Your Choice:\t";
			cin>>ch;
			switch(ch)
			{case '1':
					do{ system("cls");logo();
					cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tCustomer";
					cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t01. Add Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t02. Display Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t03. Delete Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t04. Search Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t05. Modify Record ";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t06. Add Checkout Date";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t07. Bill";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t08. Exit";
					cout<<"\n\n\t\t\t\t\t\t\t\tEnter Your Choice(1-8):\t ";
					cin>>ch;
					switch(ch)
						{
						case '1':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tAdd Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
							write_cus();
							break;
						case '2':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tDisplay Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							display_cus();
							break;
						case '3':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tDelete Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							delete_cus();
							break;
						case '4':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tSearch Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							search_cus();
							break;
						case '5':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tModify Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							modify_cus();
							break;
						case '6':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tCustomer CheckOut Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							cout<<"\n\n\t\t\t\t\t\t\t\t\tEnter The id No. : \t"; cin>>id;
						    out(id);
							break;
						case '7':	
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tBill";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\n";
						    billl();
						    break;
						case '8':
							break;
						 default :cout<<"\a";logo();
						 cout<<"\n\n\t\t\t\t\t\t\t\t\tWrong Choice\t";
					    }
					getch();
			        }while(ch!='8');
			        break;
			case '2':
					do{
					system("cls");logo();
					cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tEmployee";
					cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t01. Add Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t02. Display Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t03. Delete Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t04. Search Record";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t05. Modify Record ";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t06. Bill";
					cout<<"\n\n\t\t\t\t\t\t\t\t\t07. Exit";
					cout<<"\n\n\t\t\t\t\t\t\t\tEnter Your Choice(1-7):\t ";
					cin>>ch;
					switch(ch)
						{
						case '1':
							system("cls");logo();
								cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tAdd Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							write_emp();
							break;
						case '2':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tDisplay Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							display_emp();
							break;
						case '3':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tDelete Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n";
							cout<<"\n\n\t\t\t\t\t\t\t\t\tEnter Employee id:\t ";cin>>id;cout<<"\n\n";
							delete_emp(id);
							break;
						case '4':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tSearch Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
								cout<<"\n\n\t\t\t\t\t\t\t\t\tEnter Employee id:\t ";
								cin>>id;cout<<"\n\n";
						search_emp(id);
							break;
						case '5':
							system("cls");logo();
							cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tModify Record";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
								cout<<"\n\n\t\t\t\t\t\t\t\t\tEnter Employee id:\t ";cin>>id;
							modify_emp(id);
							break;
						case '6':	
						    system("cls");logo();
						    cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tBill";
					        cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\n\n";
						    bille();
						    break;
						case '7':
							break;
				    	default :cout<<"\a";logo();
				    	cout<<"\n\n\t\t\t\t\t\t\t\t\tWrong Choice\t";
						}
					getch();
				    }while(ch!='7');
				    break;
			case'3':
					break;
				}
		     	}while(ch!='3'); break;
		    }else
			{logo();
			cout<<"\n\n\n\t\t\tWrong Password\n\t\t\tTry Again";}
			n++;
			}while(n<2);
			break;	
	case '2':
		system("cls");
	logo();
		cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tSearch Customer Record";
		 cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
		search_cus();
		break;
	case '3':
	system("cls");
	logo();
		cout<<"\n\n\n\n\n\n\n\t\t" "\t\t\t\t\t\t\tSearch Record";
		 cout<<"\n\t" "\t\t\t\t\t\t\t\t\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\xCD\n\n";
		cout<<"\n\n\t\t\t\t\t\t\t\t\tEnter Employee id:\t ";cin>>id;cout<<"\n\n";
		search_emp(id);
		break;
	case '4':
		system("cls");logo();
		cout<<"\n\n\n\n\n\n\n\t\t\t\t\t\t\t\t\tThanks for using hotel managemnt system";
		break;
	default:
		system("cls");logo();
		cout<<"\n\n\t\t\t\t\t\t\t\t\tWrong Choice\t";
	}getch();
}while(ch!='4'); break;
}
else
{system("cls"); logo();
cout<<"\n\n\t\t\t\t\t\t\t\t\tWrong Password\n\t\t\t\t\t\t\t\t\t\tTry Again\t";}
m++;
}while(m<3);
return 0;
}
