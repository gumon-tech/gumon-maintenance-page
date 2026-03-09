# gumon-maintainance-page

หน้าแจ้งปิดปรับปรุงเซิร์ฟเวอร์ (maintenance page) แบบเรียบง่าย

`config.json`

```json
{
	"startTime": "2026-03-10T20:30:00+07:00",
	"endTime": "2026-03-11T09:30:00+07:00",
	"timezone": "Asia/Bangkok",
	"timezoneLabel": {
		"th": "(เวลาประเทศไทย, UTC+7)",
		"en": "(Thailand Time, UTC+7)"
	},
	"showTimezoneToggle": true
}
```

อธิบายฟิลด์สำคัญ
- `startTime` / `endTime`: เวลาที่แสดงบนหน้าจอ ต้องเป็น ISO8601 พร้อม timezone offset
- `timezone`: ชื่อ IANA timezone ที่ใช้เป็นค่าเริ่มต้น (เช่น `Asia/Bangkok`)
- `timezoneLabel`: ป้ายสั้น ๆ สำหรับแสดงใต้เวลาของหน้า (รองรับ `th` และ `en`)
- `showTimezoneToggle`: ค่า boolean เปิด/ปิดปุ่มสลับการแสดง timezone (true = แสดงปุ่ม, false = ซ่อนปุ่ม)

ปุ่ม timezone
- เมื่อเปิดไว้ (`showTimezoneToggle: true`) ผู้ใช้งานจะเห็นปุ่ม `TZ` ที่มุมบนขวา ใช้สลับระหว่างการแสดงเวลาตาม timezone ของผู้ชม (viewer local) กับ timezone ที่กำหนดใน `config.json`.