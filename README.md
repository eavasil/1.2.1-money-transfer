# Отчёт о тестировании приложения банковских транзаций (перевод денежных средство со счета) 

## Краткое описание

03/11/2021  было проведено тестирование приложения банковских транзакций 

На тестирование затрачено: 0.1 часа 

В результате тестирования обнаружен дефект:

Несоотвествие итоговой суммы на балансе счета после проведения пополнения. 

Ожидаемый результат: 2_500_000_000
Фактический результат:  -1794967296

## Описание процесса тестирования

В качестве тестовых данных использовались следующие данные: 

public class Main {
    public static void main(String[] args) {
        int accountBalance = 2_000_000_000;
        int transferPlus = 500_000_000;
        int currentBalance = accountBalance + transferPlus;
        System.out.println(currentBalance);
    }
}

Тестирование производилось в следующем окружении:
* Windows 10 Домашняя для одного языка 64 bit
* версия Java11 11.0.11
* Visual Studio Code
* IntelliJ IDEA Community Edition