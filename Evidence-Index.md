PT1 A series of successful pings and replies from different IP addresses, showing network connectivity. This however does not establish other IP addresses can outwardly ping, just that they can receive. This was from Cisco activity 2.1.7. <img width="874" height="1000" alt="Screenshot 2026-11-06 131359" src="https://github.com/user-attachments/assets/cb40e175-827b-44ea-8e49-f3472fefeb31" />


PT2 A tracert command showing connectivity to a service, while a ping shows a lack thereof, indicating an issue ARP cache. This establishes that there is an issue but not why the issue is occurring. This was from Cisco activity 2.1.7. <img width="838" height="842" alt="Screenshot 2026-11-06 131419" src="https://github.com/user-attachments/assets/36a8fc96-a83c-427f-a7fb-be1438dd6997" />

WS1 Wireshark capture displaying SSH capture, using a filter to display exclusively SSH packets captured. SSH packets are encrypted, which restricts information from being gathered. <img width="1920" height="1084" alt="SSH" src="https://github.com/user-attachments/assets/e196e867-2eed-4808-ab9e-7683ebc67bdd" />

WS2 Telnet packet capture, utilizing a filter to display only Telnet packets. Telnet packets are not inherently encrypted, however you also cannot say for sure what the information being transmitted is useful for. <img width="1920" height="1084" alt="Telnet filter" src="https://github.com/user-attachments/assets/3b679991-9c7b-4961-bf61-29646c975033" />

WS3 An HTTPS service being opened via FireFox browser, then being closed. There is not much to gather from a user opening a HTTPS connection, only that they have done so. <img width="1920" height="1084" alt="FirefoxOpen" src="https://github.com/user-attachments/assets/e6c57375-3642-4aa9-bddd-5b365043194b" />
