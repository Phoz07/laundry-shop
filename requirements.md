## Phase 1 Requirements
A. Functional Requirements (สิ่งที่ระบบต้องทำได้)
Navigation System (ระบบนำทาง):
[FR-01] เมนูบาร์ต้องลอยค้างอยู่ด้านบน (Sticky Header) เมื่อเลื่อนหน้าจอ
[FR-02] เมื่อกดเมนู ต้องเลื่อนลงไปยังส่วนนั้นๆ อย่างนุ่มนวล (Smooth Scroll) ไม่ใช่การเปลี่ยนหน้าใหม่
Information Display (การแสดงข้อมูล):
[FR-03] Hero Section: ต้องมีรูปภาพ/วิดีโอพื้นหลัง, Headline, และปุ่ม CTA ที่เด่นชัด
[FR-04] Pricing Table: แสดงตารางราคาแยกตามประเภท (ซักอบ/รีด/ซักแห้ง) และรองรับการดูบนมือถือ (Table Responsive)
[FR-05] Service Area: แสดงรายชื่อเขต/คอนโดที่ให้บริการ หรือแสดง Map Iframe
[FR-06] Contact: แสดงเบอร์โทรศัพท์ที่กดโทรออกได้ทันที (Link tel:) และปุ่ม Social Media
Facebook Chat Integration (ระบบแชท):
[FR-07] ต้องแสดงไอคอน Messenger ลอยอยู่ที่มุมขวาล่างของหน้าจอทุก Device
[FR-08] เมื่อกดไอคอน ต้องเปิดหน้าต่างแชทขึ้นมาโดยไม่เปลี่ยนหน้าเว็บ (Overlay)
[FR-09] ผู้ใช้ต้องสามารถเริ่มแชทได้ในฐานะ "Guest" (ไม่ต้อง Login Facebook) หากตั้งค่าไว้
[FR-10] ระบบแชทต้องโหลดขึ้นมาหลังจากหน้าเว็บหลักโหลดเสร็จแล้ว (Lazy Load) เพื่อไม่ให้เว็บช้า

B. Non-Functional Requirements (ประสิทธิภาพและคุณภาพ)
Performance:
[NFR-01] Google Lighthouse Score (Performance) ต้องมากกว่า 90 คะแนน
[NFR-02] First Contentful Paint (FCP) ต้องต่ำกว่า 1.5 วินาที
Responsiveness:
[NFR-03] การแสดงผลต้องสมบูรณ์ 100% บนมือถือ (Mobile First Design)
[NFR-04] Chat Plugin ต้องไม่บังเนื้อหาสำคัญ หรือปุ่มกดอื่นๆ บนหน้าจอมือถือ
SEO (Search Engine Optimization):
[NFR-05] ต้องมี Meta Tags ครบถ้วน (Title, Description, Open Graph สำหรับแชร์ลง Social)
[NFR-06] มี Semantic HTML (<header>, <main>, <section>, <footer>) เพื่อให้ Google Bot เข้าใจโครงสร้าง

## Technologies
Core Framework: Sveltekit
Styling: Tailwind CSS
Chat: Facebook SDK
Analytics: Google Analytics
Deployment: Cloudflare Pages