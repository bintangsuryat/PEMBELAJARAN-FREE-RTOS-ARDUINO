# PEMBELAJARAN-FREE-RTOS-ARDUINO
FreeRTOS multi-task sensor monitor on Arduino Mega - 3 concurrent tasks, UART logging, I2C

## 
**Simulation link:** https://wokwi.com/projects/466404451278666753

## Tasks

| Task | Priority | Period | Function |
|------|----------|--------|----------|
| SensorRead | 2 (High) | 1000ms | Reads temperature and humidity |
| UartLogger | 1 (Low) | 1100ms | Logs data over UART serial |
| Heartbeat | 1 (Low) | 1000ms | Blinks LED as system health indicator |

---

---

## Key Concepts Demonstrated

- FreeRTOS task creation with xTaskCreate
- Priority-based preemptive scheduling
- Inter-task communication via shared volatile variables
- vTaskDelay non-blocking delays using portTICK_PERIOD_MS
- UART serial logging at 115200 baud
- I2C peripheral initialisation with Wire.begin()
