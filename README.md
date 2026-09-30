# DeepLearning
# 🐱🐶 CNN Bias Analysis: Shape vs. Texture in ResNet18

โปรเจกต์นี้เป็นส่วนหนึ่งของการศึกษาและทดลองรายวิชา Deep Learning เพื่อตรวจสอบพฤติกรรมการตัดสินใจและวิเคราะห์ความเอนเอียง (Bias) ของโมเดล Convolutional Neural Network (CNN) สถาปัตยกรรม **ResNet18** ว่ามีน้ำหนักความเอนเอียงไปทางรูปทรง (Shape) หรือพื้นผิวและลวดลาย (Texture) 

## 📌 สรุปภาพรวม (Project Overview)
การทดลองนี้แบ่งการฝึกสอนโมเดลออกเป็น 2 รูปแบบเพื่อเปรียบเทียบกัน:
1. **Baseline Model:** ฝึกสอนด้วยภาพสุนัขกับแมว
2. **Shape-Biased Model:** ฝึกสอนด้วยภาพลายเส้นขอบที่ผ่านกระบวนการ Canny Edge Detection (บังคับให้โมเดลเรียนรู้เฉพาะรูปทรง)

หลังจากฝึกสอนสำเร็จ ได้ทำการทดสอบโมเดลด้วย **ภาพความขัดแย้ง (Cue Conflict)** เช่น ภาพโครงร่างของแมวที่ถูกซ้อนทับด้วยลวดลายของม้าลาย เพื่อวิเคราะห์ว่าโมเดลใช้ปัจจัยใดเป็นหลักในการจำแนกภาพ

## 📂 ชุดข้อมูล (Dataset)
* **ชื่อชุดข้อมูล:** Cats and Dogs
* **แหล่งที่มา:** [Kaggle Dataset](https://www.kaggle.com/datasets/marquis03/cats-and-dogs) (หรือ Microsoft Asirra)
* **สัญญาอนุญาต (License):** Apache 2.0 / Open for Academic Use

## 🚀 วิธีการรันโค้ด (How to Run)
โปรเจกต์นี้เขียนและทดสอบบน **Google Colab** โดยมีการตั้งค่า `set_seed(42)`
1. เปิดไฟล์ `Model_Deep.ipynb` บน Google Colab
2. ไปที่เมนู **Runtime** > **Chang runtime** > **เปลี่ยนเป็น T4GPU**
3. กดรันทีละ cell เนื่องจากต้องใช้เวลารันแต่ละโค้ด ลดข้อผิดพลาด
