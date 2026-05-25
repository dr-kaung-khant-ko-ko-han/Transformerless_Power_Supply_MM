# Transformerless_Power_Supply_MM

Transformerless Power Supply (Capacitive Power Supply) ဒီဇိုင်းလမ်းညွှန်
Transformerless Power Supply (TPS) သို့မဟုတ် Capacitive Power Supply ဆိုသည်မှာ AC Main Voltage ကို လိုအပ်သော DC Voltage အနိမ့်သို့ ပြောင်းလဲပေးရာတွင် သမားရိုးကျ Transformer ကို အသုံးမပြုဘဲ Capacitive Reactance ကို အသုံးပြု၍ Current ကို ကန့်သတ်ကာ ဗို့အားကို လျှော့ချပေးသော Power Supply အမျိုးအစား ဖြစ်ပါသည်။ ၎င်းသည် အရွယ်အစား သေးငယ်ခြင်း၊ အလေးချိန် ပေါ့ပါးခြင်းနှင့် ကုန်ကျစရိတ် သက်သာခြင်းတို့ကြောင့် LED မီးများ၊ အာရုံခံကိရိယာများ (Sensors) နှင့် အခြား Low-Current လိုအပ်သော Circuit များတွင် အသုံးများပါသည်။

၁။ Capacitive Power Supply ၏ အလုပ်လုပ်ပုံ အခြေခံသဘောတရား
TPS ၏ အဓိက အလုပ်လုပ်ပုံမှာ Series Capacitor (C1) ကို အသုံးပြု၍ AC Mains Voltage ကို လျှော့ချခြင်း ဖြစ်သည်။ Transformer သည် Magnetic Field ကို အသုံးပြု၍ ဗို့အားကို လျှော့ချသော်လည်း၊ Capacitor သည် ၎င်း၏ Capacitive Reactance ($X_c$) ကို အသုံးပြု၍ Current ကို ကန့်သတ်ခြင်းဖြင့် ဗို့အားကို လျှော့ချပါသည်။

Capacitor သည် AC Circuit တွင် Resistance ကဲ့သို့ ပြုမူသော်လည်း၊ ၎င်းသည် Power ကို အပူအဖြစ် စွန့်ထုတ်ခြင်း မရှိဘဲ Energy ကို သိမ်းဆည်းခြင်းနှင့် ပြန်လွှတ်ခြင်းသာ ပြုလုပ်သောကြောင့် Power Loss နည်းပါးပါသည်။

Voltage Dropping Capacitor (C1)
အချက်အလက်	ရှင်းလင်းချက်
အသုံးပြုရခြင်း အကြောင်းရင်း	AC Mains Voltage ကို လိုအပ်သော Current ပမာဏအထိ ကန့်သတ်ရန်နှင့် ဗို့အားကို လျှော့ချရန်။
အလုပ်လုပ်ပုံ	Capacitor ၏ Reactance ($X_c$) သည် AC Mains Voltage ၏ အများစုကို ၎င်းကိုယ်တိုင်ပေါ်တွင် ကျဆင်းစေပြီး၊ Load သို့ စီးဆင်းမည့် Current ကို ကန့်သတ်ပေးသည်။
တွက်ချက်ပုံ (Design)	Capacitor ၏ တန်ဖိုးသည် Circuit မှ လိုအပ်သော Output Current ($I_{out}$) ပေါ်တွင် မူတည်ပါသည်။
တွက်ချက်ရန် ဖော်မြူလာများ

၁။ Capacitive Reactance ($X_c$) တွက်ချက်ခြင်း:

$$
X_c = \frac{1}{2 \pi f C}
$$

$X_c$ = Capacitive Reactance (Ohms)

$f$ = AC Mains Frequency (Hz) (ဥပမာ: မြန်မာနိုင်ငံတွင် 50 Hz)

$C$ = Capacitor Value (Farads)

၂။ လိုအပ်သော Reactance ($X_c$) တွက်ချက်ခြင်း:

Circuit မှ လိုအပ်သော Current ($I_{out}$) ကို ရရှိရန်အတွက် လိုအပ်သော $X_c$ ကို အောက်ပါအတိုင်း တွက်ချက်နိုင်ပါသည်။

$$
X_c \approx \frac{V_{in(RMS)}}{I_{out}}
$$

$V_{in(RMS)}$ = AC Mains RMS Voltage (ဥပမာ: 230V)

$I_{out}$ = Circuit မှ လိုအပ်သော Current (Amperes)

၃။ Capacitor တန်ဖိုး ($C$) တွက်ချက်ခြင်း:

အထက်ပါ $X_c$ တန်ဖိုးကို အသုံးပြု၍ $C$ ကို တွက်ချက်နိုင်ပါသည်။

$$
C = \frac{1}{2 \pi f X_c}
$$

ဥပမာ တွက်ချက်မှု:

$V_{in(RMS)} = 230V$

$f = 50Hz$

$I_{out} = 20mA$ (သို့မဟုတ် 0.02A)

$$
X_c \approx \frac{230V}{0.02A} = 11,500 \Omega
$$

$$
C = \frac{1}{2 \times 3.14159 \times 50 \times 11,500} \approx 2.77 \times 10^{-7} F \approx 0.277 \mu F
$$

မှတ်ချက်: C1 အတွက် X2-rated Metallized Polypropylene Capacitor ကိုသာ အသုံးပြုရမည်။ ၎င်းသည် AC Mains Voltage ကို ခံနိုင်ရည်ရှိပြီး Safety Standard နှင့် ကိုက်ညီပါသည်။

၂။ Bleeder Resistor (R1 - 1/4W)
အချက်အလက်	ရှင်းလင်းချက်
အသုံးပြုရခြင်း အကြောင်းရင်း	ဘေးကင်းလုံခြုံရေး (Safety) အတွက် အဓိက အသုံးပြုပါသည်။ Power Supply ကို AC Outlet မှ ဖြုတ်လိုက်သည့်အခါ Capacitor (C1) တွင် ဗို့အား မြင့်မားစွာ ကျန်ရှိနေနိုင်ပြီး ၎င်းကို ထိမိပါက လျှပ်စစ်ရှော့ခ် ဖြစ်နိုင်ပါသည်။ R1 သည် ၎င်းကျန်ရှိနေသော ဗို့အားကို အချိန်တိုအတွင်း လျှပ်စစ်ဓာတ်ကုန်စေရန် (Discharge) အတွက် C1 နှင့် Parallel ဆက်ထားခြင်း ဖြစ်ပါသည်။
အလုပ်လုပ်ပုံ	Power ဖြတ်တောက်ပြီးနောက် C1 တွင် သိုလှောင်ထားသော Energy ကို R1 မှတဆင့် အပူအဖြစ် စွန့်ထုတ်ပေးပါသည်။
တွက်ချက်ပုံ (Design)	R1 ၏ တန်ဖိုးကို Discharge Time Constant ပေါ် မူတည်၍ ရွေးချယ်ပါသည်။
R1 တန်ဖိုး ရွေးချယ်ခြင်း:

တန်ဖိုး မြင့်မားသော Resistor (ဥပမာ: ၄၇၀kΩ မှ ၁MΩ) ကို ရွေးချယ်လေ့ရှိသည်။
တန်ဖိုး မြင့်မားခြင်းကြောင့် ပုံမှန် အလုပ်လုပ်နေစဉ်အတွင်း Power Loss ($P = V^2/R$) အလွန်နည်းပါးစေသည်။
Power Rating: $V_{in(RMS)} = 230V$ နှင့် $R = 1M\Omega$ အတွက် Power Dissipation မှာ $P = 230^2 / 1,000,000 \approx 0.053W$ သာ ရှိသောကြောင့် 1/4W Resistor သည် လုံလောက်ပါသည်။

၃။ Surge Limiting Resistor (R2 - 2W)
အချက်အလက်	ရှင်းလင်းချက်
အသုံးပြုရခြင်း အကြောင်းရင်း	Circuit ကို စတင်ဖွင့်လိုက်သည့်အခါ (Switch-On) တွင် Capacitor (C1) သည် ခဏတာမျှ Short Circuit ကဲ့သို့ ပြုမူသောကြောင့် Inrush Current (Surge Current) အလွန်မြင့်မားစွာ စီးဆင်းနိုင်ပါသည်။ ဤ Surge Current သည် Rectifier Diode များနှင့် Zener Diode များကို ပျက်စီးစေနိုင်သောကြောင့် ၎င်းကို ကန့်သတ်ရန်အတွက် R2 ကို C1 နှင့် Series ဆက်ထားခြင်း ဖြစ်ပါသည်။
အလုပ်လုပ်ပုံ	စတင်ဖွင့်ချိန်တွင် R2 သည် ယာယီအားဖြင့် Current ကို ကန့်သတ်ပေးပြီး၊ ပုံမှန် အလုပ်လုပ်ချိန်တွင်မူ ၎င်း၏ Resistance တန်ဖိုး နည်းပါးသောကြောင့် Power Loss အနည်းငယ်သာ ရှိပါသည်။
တွက်ချက်ပုံ (Design)	R2 ၏ တန်ဖိုးသည် Surge Current ကို ကန့်သတ်ရန်နှင့် ပုံမှန် Current စီးဆင်းမှုကို မထိခိုက်စေရန်အတွက် နည်းပါးသော တန်ဖိုးကို ရွေးချယ်ပါသည်။
R2 တန်ဖိုး ရွေးချယ်ခြင်း:

တန်ဖိုး နည်းသော Resistor (ဥပမာ: ၁၀Ω မှ ၁၀၀Ω) ကို ရွေးချယ်လေ့ရှိသည်။
Power Rating: Surge Current သည် အလွန်မြင့်မားပြီး ခဏတာ ဖြစ်သော်လည်း၊ Resistor သည် ထို Peak Power ကို ခံနိုင်ရည်ရှိရန် လိုအပ်ပါသည်။ ထို့ကြောင့် 1W သို့မဟုတ် 2W Resistor ကို အသုံးပြုရန် လိုအပ်ပါသည်။

၄။ Output Voltage နှင့် Current ဒီဇိုင်း
Transformerless Power Supply ၏ Output ကို ဒီဇိုင်းလုပ်ရာတွင် အဓိက အချက်နှစ်ချက် ရှိပါသည်။

Output Current ($I_{out}$) တွက်ချက်ပုံ
Output Current ကို အဓိကအားဖြင့် Voltage Dropping Capacitor (C1) ၏ တန်ဖိုးဖြင့်သာ ကန့်သတ်ထားပါသည်။

$$
I_{out(max)} \approx \frac{V_{in(RMS)}}{X_c}
$$

Circuit မှ လိုအပ်သော Current ကို ဦးစွာ သတ်မှတ်ပါ။ ဥပမာ: 20mA လိုအပ်ပါက၊ C1 ကို 20mA ထုတ်ပေးနိုင်ရန် တွက်ချက်ရမည်။
Zener Diode နှင့် Load တို့သည် ဤ Current ကို မျှဝေယူကြမည် ဖြစ်သည်။
Output Voltage ($V_{out}$) တွက်ချက်ပုံ
Output Voltage ကို Zener Diode ကို အသုံးပြု၍ ထိန်းချုပ်ပါသည်။

Zener Diode (Z1): Rectifier Bridge ၏ Output နှင့် Parallel ဆက်ထားသော Zener Diode သည် Output Voltage ကို ၎င်း၏ Zener Voltage ($V_z$) တန်ဖိုးတွင် တည်ငြိမ်အောင် ထိန်းချုပ်ပေးပါသည်။
$V_{out} = V_z$ ဖြစ်ပါသည်။
Filter Capacitor (C2): Zener Diode နှင့် Parallel ဆက်ထားသော Electrolytic Capacitor (C2) သည် Rectified DC တွင် ကျန်ရှိနေသော Ripple ကို လျှော့ချပေးပြီး Output ကို ပိုမို ပြေပြစ်စေပါသည်။
Zener Diode အတွက် Current တွက်ချက်ခြင်း:

Zener Diode နှင့် Load တို့သည် C1 မှ ထုတ်ပေးသော စုစုပေါင်း Current ($I_{out}$) ကို မျှဝေယူပါသည်။

$$
I_{out} = I_{load} + I_{zener}
$$

$I_{load}$ = Load မှ လိုအပ်သော Current

$I_{zener}$ = Zener Diode မှ စီးဆင်းသော Current (တည်ငြိမ်စေရန်အတွက် $I_{zener}$ သည် အနည်းဆုံး $5mA$ ခန့် ရှိသင့်သည်)

ဒီဇိုင်း အဆင့်ဆင့် အကျဉ်းချုပ်

အဆင့်	လုပ်ဆောင်ချက်	တွက်ချက်ပုံ

၁။ Output သတ်မှတ်ခြင်း	လိုအပ်သော $V_{out}$ နှင့် $I_{load}$ ကို သတ်မှတ်ပါ။	$V_{out} = V_z$
၂။ စုစုပေါင်း Current	$I_{out} = I_{load} + I_{zener(min)}$ ကို တွက်ပါ။	$I_{out}$ (ဥပမာ: $20mA$)
၃။ Dropping Capacitor	$I_{out}$ ကို အသုံးပြု၍ $X_c$ နှင့် $C$ တန်ဖိုးကို တွက်ပါ။	$C = \frac{I_{out}}{2 \pi f V_{in(RMS)}}$
၄။ Bleeder Resistor	$470k\Omega$ မှ $1M\Omega$ (1/4W) ကို ရွေးချယ်ပါ။	$R1 \approx 1M\Omega$
၅။ Surge Resistor	$10\Omega$ မှ $100\Omega$ (1W သို့မဟုတ် 2W) ကို ရွေးချယ်ပါ။	$R2 \approx 47\Omega$ (2W)
၅။ အရေးကြီးသော ဘေးကင်းလုံခြုံရေး သတိပေးချက်

Transformerless Power Supply ၏ အကြီးမားဆုံး အားနည်းချက်မှာ Galvanic Isolation မရှိခြင်း ဖြစ်ပါသည်။ ဆိုလိုသည်မှာ Circuit တစ်ခုလုံးသည် AC Mains Voltage နှင့် တိုက်ရိုက် ချိတ်ဆက်နေပြီး "Live" ဖြစ်နေပါသည်။

Circuit ကို ကိုင်တွယ်ခြင်း၊ စမ်းသပ်ခြင်းနှင့် အသုံးပြုခြင်းတို့တွင် လျှပ်စစ်ရှော့ခ် အန္တရာယ် အလွန်မြင့်မားသောကြောင့် အထူးသတိထားရန် လိုအပ်ပါသည်။
ဤ Power Supply အမျိုးအစားကို User မှ တိုက်ရိုက် ထိတွေ့နိုင်သော (Non-Isolated) Application များတွင် လုံးဝ အသုံးမပြုသင့်ပါ။
Bleeder Resistor (R1) ကို မဖြစ်မနေ အသုံးပြုရမည်။
