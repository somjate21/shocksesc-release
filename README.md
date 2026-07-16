# ShockSESC – Release / OTA

ช่องทางอัปเดตออนไลน์ (OTA) ของแอป ShockSESC

- แอปอ่าน [`version.json`](version.json) เพื่อเช็คเวอร์ชันใหม่
- ไฟล์ติดตั้ง `.apk` แนบไว้ที่หน้า [Releases](../../releases)

## วิธีปล่อยอัปเดตใหม่
1. เพิ่มเลขเวอร์ชันใน `pubspec.yaml` ของแอป (เช่น `1.0.1+2`) แล้ว build:
   `flutter build apk --release`
2. สร้าง release ใหม่ + อัปโหลด APK:
   `gh release create v1.0.1 "path/to/app-release.apk#ShockSESC.apk" -t "v1.0.1" -n "รายละเอียด"`
3. แก้ `version.json` ให้ `version` และ `apk_url` ชี้เวอร์ชันใหม่ แล้ว commit + push
4. เครื่องลูกค้าจะเด้งแจ้งเตือนในหน้า Settings เอง
