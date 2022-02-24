![image](https://user-images.githubusercontent.com/90384405/155476061-69c1e6c6-7253-405d-9a3d-7cdd486ea7c0.png)
![image](https://user-images.githubusercontent.com/90384405/155476077-0de0dcac-0710-48dd-84de-eab9340c1f71.png)
![image](https://user-images.githubusercontent.com/90384405/155476094-a3196460-d100-4de8-858a-cb6b231ad803.png)
![image](https://user-images.githubusercontent.com/90384405/155476103-8a6d8eab-515c-4183-b9ce-3588d092afcc.png)
![image](https://user-images.githubusercontent.com/90384405/155476126-a0cd9677-856c-4d6d-80e5-29d316400401.png)
![image](https://user-images.githubusercontent.com/90384405/155476139-0fe75b04-64d3-41d8-886c-d53e501f9523.png)
![image](https://user-images.githubusercontent.com/90384405/155476155-7a1cc98d-e8fb-4a34-80b4-dc43317d28a2.png)
![image](https://user-images.githubusercontent.com/90384405/155476165-ea963063-3f0a-4181-bb58-74c896908daf.png)
![image](https://user-images.githubusercontent.com/90384405/155476180-84a1a93b-ecf5-4842-b64b-9c24a4cf4dc2.png)
![image](https://user-images.githubusercontent.com/90384405/155476194-d28a1d09-0b2b-480c-b6e6-ff07404b4557.png)
![image](https://user-images.githubusercontent.com/90384405/155476205-8423e7b6-2f75-4a58-9097-1e9cbe1106b6.png)
В функции `thread_worker` опишем работу с потоками. Подключаемся для каждого потока к нашей БД, определяем нашу позицию с помощью класса `Cursor` и создадим файл для записи с именем res_Номер потока_False, где False означает, что вначале рассматривается использование буфера. Пока мы проходим по всем строкам с помощью запроса `SELECT * FROM ticket_flights_tmp WHERE id={pos}`. Метод `.fetchone()` возвращает первую запись, полученную при запросе и мы записываем ее в файл
![image](https://user-images.githubusercontent.com/90384405/155476256-808b73da-31d2-49c0-a892-f832704871b1.png)
![image](https://user-images.githubusercontent.com/90384405/155476277-436e6b13-6a87-4fe1-9a72-7e1ee094b9f6.png) ![image](https://user-images.githubusercontent.com/90384405/155476293-67345c66-6c61-4031-838e-31a2da602787.png)
Первое прохождение - 62.98392415046692 s Второе прохождение - 112.37231516838074 s. Время увеличилось, так как мы уведомляем систему что надо записать на диск, и не использовать буфер.
![image](https://user-images.githubusercontent.com/90384405/155476330-cca61e2a-2fdb-4d36-a357-e564a7726c64.png)
`True:`
![image](https://user-images.githubusercontent.com/39220694/154050444-942d6cbd-05da-46aa-986c-10f41556111a.png)

