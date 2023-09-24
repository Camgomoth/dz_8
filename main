from datetime import date, datetime


def get_birthdays_per_week(list):
    dates = []
    now = datetime.today().date()
    result = {}
    monday_list = []
    tuesday_list = []
    wednesday_list = []
    thursday_list = []
    friday_list = []
   

    



    
    for i in list:
        years = timedelta(now.year - i.get('birthday').year)
       
        diff =  now - i.get('birthday')
        if i.get('birthday').month == now.month:
            if i.get('birthday').day >= now.day and i.get('birthday').day < (now.day + 7) :
                dates.append(i['birthday'] + years)
        if i.get('birthday').month > now.month:
            if (int(diff.days - ((((now.year - i.get('birthday').year)-((now.year - i.get('birthday').year)/4))*365)+((((now.year - i.get('birthday').year)/4))*366)))) > -7 and\
            (int(diff.days - ((((now.year - i.get('birthday').year)-((now.year - i.get('birthday').year)/4))*365)+((((now.year - i.get('birthday').year)/4))*366)))) < 0:
                 dates.append(i['birthday'] + years)
       
    for i in dates:
        if i.weekday() == 0 or i.weekday() == 5 or i.weekday() == 6:
            name = list[dates.index(i)].get('name').find(' ')
            
            monday_list.append(list[dates.index(i)].get('name')[:name])


            
            
        
        if i.weekday() == 1:
            name = list[dates.index(i)].get('name').find(' ')
            
            tuesday_list.append(list[dates.index(i)].get('name')[:name])


            
            
        
        if i.weekday() == 2:
            name = list[dates.index(i)].get('name').find(' ')
            
            wednesday_list.append(list[dates.index(i)].get('name')[:name])


            
           

        if i.weekday() == 3:
            name = list[dates.index(i)].get('name').find(' ')
            
            thursday_list.append(list[dates.index(i)].get('name')[:name])


            
            
    
        
        if i.weekday() == 4:
            name = list[dates.index(i)].get('name').find(' ')
            
            friday_list.append(list[dates.index(i)].get('name')[:name])


            
            
        
        result["Monday"] = monday_list
        result["Tuesday"] = tuesday_list
        result["Wednesday"] = wednesday_list
        result["Thursday"] = thursday_list
        result["Friday"] = friday_list

        

    return result


if __name__ == "__main__":
    users = [
        {"name": "Jan Koum", "birthday": datetime(1976, 1, 1).date()},
    ]

    result = get_birthdays_per_week(users)
    print(result)
    # Виводимо результат
    for day_name, names in result.items():
        print(f"{day_name}: {', '.join(names)}")
