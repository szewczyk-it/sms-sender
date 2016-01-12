# sms-sender
Simple sms getway to sending sms by Huawei E3372 HiLink

Tested on:
- Linux Mint - works fine
- Cygwin - works, but have problems with codepage UTF-8 (accented characters like ęół etc.)

```	
	USAGE:
	sms.sh -t|--to <dest_number> -m|--message <message> [-i|--ip <ip>] [-a|--accent] [-l|--log <log_file>]
		-t|--to dest_number
			Receiver phone number or numbers separated by comma (,) eg. 123456789,987654321.
		-m|--message message
			Message to send.
		-i|--ip ip
			[optional] Custom ip of the modem (default is 192.168.8.1).
		-a|--accent
			[optional] Message with international characters. Without it characters like 'ęó' will be changed to 'eo'.
		-l|--log log_file
			[optional] File to logging.
			
	Environment variables:
		SMS_NUMBERS- the same as --to
		SMS_MESSAGE    - the same as --message
		SMS_IP     - the same as --ip
		SMS_ACCENT - any non empty string, the same as --accent
		SMS_LOG    - the same as --log
	Environment variables will be overwritten by command line parameters.

	Exit codes:
		0 - OK
		1 - command line errors
		2 - modem not available
		3 - sending failed
```
