idf_component_register(SRCS "main.c"
		"config.c"
		"core_dump.c"
		"log.c"
		"interface/ntrip_util.c"
		"retry.c"
		"status_led.c"
		"stream_stats.c"
		"uart.c"
		"util.c"
		"web_server.c"
		"wifi.c"
		"interface/ntrip_server.c"
		"interface/ntrip_server_2.c"

		"protocol/nmea.c"
        INCLUDE_DIRS "include"
		REQUIRES esp_netif app_update driver esp_wifi nvs_flash espcoredump tcp_transport esp_http_server mbedtls json vfs spiffs lwip button)

spiffs_create_partition_image(www ../www FLASH_IN_PROJECT)
