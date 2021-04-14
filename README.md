Download

<h4>Build 33</h4>
- oprava prace s kruhovym bufferm kdyz se zprava rozdely na vice casti

<h4>Build 34</h4>
- pozicovani CU_Payload_Length

<h4>Build 35</h4>
<h5>ESP</h5>
- navýšeni stacku pro websocket z 2000 -> 4000
- oprava zobrazeni baterie pro monitor
<h5>STM</h5>
- pridane vypisy

<h4>Build 36</h4>
<h5>ESP</h5>
- oprava RX bufferu
- posilani signalu
<h5>STM</h5>
- oprava RX bufferu
- posilani signalu

<h4>Build 37</h4>
<h5>ESP</h5>
- blize nespecifikovane upravy Honzi S. na reconect Wifi

<h4>Build 38</h4>
<h5>ESP</h5>
- oprava posilani Impedance, Napeti zeme, Oprava Faults
<h5>STM</h5>
- oprava posilani Impedance, Napeti zeme, Oprava Faults
- zahrnuti uprav pro advance setup

<h4>Build 39</h4>
<h5>ESP</h5>
- Novy SW pro STM
<h5>STM</h5>
- oprava bugu na silny signalu
- oprava BarLine
- oprava navratu obrazovky po remotePairing

<h4>Build 40</h4>
<h5>ESP</h5>
- predelani blokovani odesilani logu na chyby na serveru
- 20 sec timeout na blok serveru
- nova verze STM
<h5>STM</h5>
- oprava posilani stejneho PackageId
- OutOfRange je nastavovan pres = a ne pres |=
- oprava dat z energy

<h4>Build 41</h4>
<h5>ESP</h5>
- nova verze STM
*json_parser.c*

- pri eventu LOG_CREATED, Internal server error, ostatnich errorech  se posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

*rs232.c*

- oprava posilani "--" na VOLTAGE_FENCE
- oprava posilani "--" na LOW_THRESHOLD
- oprava posilani "--" na SET STATE

*rs232.h*

- novy CMD ->RS232_TX_CMD_LOG_FINISHED					0x1B
*timers.c*

- pri timeoutu 20 sec na odpoved pri logu posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

<h5>STM</h5>

*json_parser.c*

- pri eventu LOG_CREATED, Internal server error, ostatnich errorech  se posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

*rs232.c*

- oprava posilani "--" na VOLTAGE_FENCE
- oprava posilani "--" na LOW_THRESHOLD
- oprava posilani "--" na SET STATE

*rs232.h*

- novy CMD ->RS232_TX_CMD_LOG_FINISHED					0x1B

*timers.c*

- pri timeoutu 20 sec na odpoved pri logu posila do STM log finished cimz se odblokovava komunikace na refresh hodnot

<h4>Build 42</h4>
<h5>ESP</h5>
<h5>STM</h5>

<i><b>Cloud_Uart</i></b>

- pokud se resetuje ESP behem vybirani quelle -> Neodesle se nic a na RTT se vypise log
- pridavani zprav do RTT -> CMD_END_CONFIG
- pokud je FrameCounter == 1 je na cloud posilan opakovace (jako jedinny)
- pokud CU_Payload_Length > 100 do RTT se vypise Error

<i><b>ProcessCoreTask.c</i></b>

- Pokud se odesila Our Of Range posila se s FrameCounterem = 1

<i><b>TaskCore.c</i></b>

- Out of range se posila v pripade ze zadne jine zarizeni neposila, co kazdych 15 minut

<i><b>proced.h</i></b>

- cteni HW verze desky

<i><b>main.c</i></b>

- globalni promenna HW_Version

<i><b>Update submodul SX1262 - 1.04</i></b>

- podpora noveho krystalu pro desky GAT01-RFS-08

<h4>Build 42</h4>
<h5>ESP</h5>
- novy build <b>stm 1.96</b>
<h5>STM</h5>

- oprava timeoutu nekomunikace se slavy
- pridani rolovani textu
- oprava posilani signalu
- oprava posilani impedance
- pridane posilani nazvu do radia

<h4>Build 44</h4>
<h5>ESP</h5>
- build 0.35
- bugfix memcpy zaporneho cisla

<h5>STM - ASW : build 2.00</h5>

<i><b>LCDTask</i></b>

- uprava grafiky aby se zobrazila sila prijateho testovaciho signalu

<i><b>TaskCore</i></b>

- Zakazani  generovani "nahodne" mac adresy v pripade 0 ulozene -> reseno primov bootloaderu

<i><b>TaskCloud</i></b>

- oprava pretypovani pointru (kvuli warningu)

<i><b>Cloud Uart</i></b>

- includovani watchdog controleru iwdg.h
- zapis SSID + PASSW probiha pres cyklus + obnova watchdogu
- pokud jsem na strankach QR_AP_SCEEN + QR_ADD_SCREEN a dojde k pripojeni na wifi stranka se zavre
- Odstraneni nepouzivane fce CU_Rx_CMD_Parsing

<h5>STM - BSW : build 2.16</h5>

- vypisy chyb 
- HW 0x81 - MAC 0
- HW 0x82 - MAC Spatny format
- HW 0x83 - MAC reserva
- HW 0x41 - ASW version 0
- HW 0x42 - CRC wrong
- zobrazeni MAC adresy
- zobrazeni ze se jedna o CRC skipera


<h4>Build 44</h4>

<h5>ESP</h5>

<h5>STM - ASW : build 2.01</h5>

- zapnuti WatchDogu

<h4>Build 45</h4>

<h5>ESP</h5>

<h5>STM - ASW : build 2.01</h5>

- vypnuti WatchDogu

<h4>Build 46</h4>

<h5>ESP</h5>

- pridani prepinace na devel / release sandbox

<h5>STM - ASW : build 2.10</h5>

- implementace vetve 426, 422


<h4>Build 48</h4>

<h5>ESP 38</h5>

- Pridani moznosti pripojit se k nezabezpecene wifi

<h5>STM - ASW : build 2.20</h5>

- implementace vetve 431,435,433,434


<h4>Build 49</h4>

<h5>ESP 39</h5>

- Oprava pro Pepuv mobil (long header)

<h5>STM - ASW : build 2.21</h5>

- implementace vetve 436


<h4>Build 50</h4>

<h5>ESP 39</h5>

<h5>STM - ASW : build 2.22</h5>

- implementace vetve 438
- popisky ke QR kodu

<h5>STM - BSW : build 2.17</h5>

- implementace spravy napeti


<h4>Build 51</h4>

<h5>ESP 40</h5>
- novy kryptovaci klic

-nahodne cislo

<h5>STM - ASW : build 2.23</h5>

- implementace vetve 440
- sleep mode
- novy kryptovaci klic

<h5>STM - BSW : build 2.18</h5>

- implementace vetve 441
- novy kryptovaci klic



<h4>Build 52</h4>

<h5>ESP 41</h5>
- zrychleni poslani zmeny


<h4>Build 53</h4>

<h5>ESP 42</h5>
- uprava rychlosti posilani

<h5>STM - ASW : build 2.24</h5>

- implementace vetve 442, 443
- oprava powerManagmentu
- oprava rolovani textu
- doplneni textu pro Blocking log, RQ Blocking log

<h5>STM - BSW : build 2.19</h5>

- oprava zapisu do eeprom


<h4>Build 54</h4>

<h5>ESP 42</h5>
- aktualizace submodul

<h5>STM - ASW : build 2.25</h5>

- zobrazeni mac


<h4>Build 55</h4>

<h5>ESP 43</h5>

- implementace vetve 446

<h5>STM - ASW : build 2.26</h5>

- implementace vetve 445


<h4>Build 56</h4>

<h5>ESP 44</h5>

- pridani impedance MIN, impedance MAX, oprava delky websocket

<h5>STM - ASW : build 2.27</h5>

- implementace vetve 447


<h4>Build 57</h4>

<h5>STM - ASW : build 2.30</h5>

- implementace vetve 449


<h4>Build 58</h4>

<h5>STM - ASW : build 2.31</h5>

- implementace vetve 452, 450

<h5>STM - BSW : build 2.20</h5>


<h4>Build 59</h4>

<h5>STM - ASW : build 2.32</h5>

- oprava -> nabidka na novou MAC se zobrazovala na spatnem miste



- oprava masky


<h4>Build 60 </h4>

<h5>STM - ASW : build 2.40</h5>
- 12 zarizeni
- upgrade pres websocket

<h5>ESP</h5>
- 12 zarizeni
- certifikat pro AWS
- overivani certifikatu
- priprava na poslani klice po ws
- sntp

<h4>Build 61 </h4>

<h5>STM - ASW : build 2.41</h5>
- oprava zobrazeni main screen

<h4>Build 62 </h4>

<h5>ESP 46</h5>
- navýšení buffer

<h4>Build 63 </h4>

<h5>STM - ASW : build 2.42</h5>
- Slava test
- mazani spatne oznaceni
- spatne rolovani v main menu
- podparovani monitoru
- spatne oznaceni

<h4>Build 64 </h4>

<h5>STM - ASW : build 2.43</h5>
- oprava mazani

















