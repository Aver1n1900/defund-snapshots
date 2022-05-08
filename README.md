![image](https://user-images.githubusercontent.com/104348282/166724700-f34d905c-2b94-49ff-a09d-5942958aecc7.png)
# defund-snapshots (Нода начинает синхронизацию с 225 000 блока)
Snapshot installation May 6</br> 
**(Перед установкой рекомендуется сохранить важные файлы)**
</br>
</br>
Откройте терминал:</br>
Загрузите архив (Уходит примерно час. Командой df -h /home проверьте память должно быть свободно хоть 20%)</br>
`wget dragonapi.space/data_06052022.tar`</br>
Стопаем ноду</br>
`systemctl stop defund && defundd tendermint unsafe-reset-all`</br>
Перемещаем архив в директорию .defund</br>
`mv data_06052022.tar $HOME/.defund/`</br>
Открываем</br>
`cd $HOME/.defund/`</br>
Разархивируем её (Минут 10)</br>
`tar xfv data_06052022.tar`</br>
Загружаем addrbook.json и двигаем в директорию .defund/config/</br>
`wget dragonapi.space/addrbook.json && mv addrbook.json $HOME/.defund/config/`</br>
Стартуем, я сказала стартуем:
`sudo systemctl start defund && sudo journalctl -u defund.service -f -o cat`</br>
Открываем директорию для удаления загруженного архива </br>
`cd $HOME/.defund && rm -rf data_06052022.tar`</br>

И спасибо ему: **icodragon#4560**

