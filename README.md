# 🎄 Interactive Christmas Tree

Cây thông Noel 3D tương tác với điều khiển bằng cử chỉ tay, sử dụng Three.js và MediaPipe Hand Tracking.

## ✨ Tính năng

- **🎨 Particle System 3D**: 4000+ particles với hiệu ứng bloom và lighting chuyên nghiệp
- **👋 Hand Gesture Control**: Điều khiển bằng cử chỉ tay qua webcam
- **📷 Photo Upload**: Thêm ảnh của bạn vào cây thông 3D
- **🎵 Background Music**: Music player với Jingle Bells và volume control
- **🎭 3 Chế độ hiển thị**:
  - 🎄 **TREE Mode**: Particles tạo hình cây thông xoay tròn
  - ✨ **SCATTER Mode**: Particles phân tán trong không gian 3D
  - 🔍 **FOCUS Mode**: Phóng to và focus vào một ảnh cụ thể

## 🎮 Cách sử dụng

### Mở ứng dụng
1. Mở file `noel_v2.html` trong trình duyệt (khuyến nghị Chrome/Edge)
2. Cho phép truy cập camera khi được hỏi
3. Chờ loading hoàn tất

### Điều khiển bằng cử chỉ tay

| Cử chỉ | Chức năng | Mô tả |
|--------|-----------|-------|
| ✊ **Nắm tay** | TREE Mode | Thu nhỏ ngón tay lại - particles tạo hình cây thông |
| ✋ **Mở rộng bàn tay** | SCATTER Mode | Dang rộng tay - particles phân tán xung quanh |
| 🤏 **Chụm ngón** | FOCUS Mode | Chụm ngón cái và ngón trỏ - focus vào một ảnh ngẫu nhiên |
| 👈👉 **Di chuyển tay** | Xoay | Di chuyển tay trái/phải để xoay scene (trong SCATTER mode) |

### Thêm ảnh
1. Click nút **"Thêm ảnh"** ở giữa màn hình
2. Chọn một hoặc nhiều ảnh từ máy tính
3. Ảnh sẽ xuất hiện trong cây thông với khung vàng đồng

### 🎵 Nhạc nền
Ứng dụng có music player với Jingle Bells (hoặc nhạc Noel miễn phí):

1. **Phát nhạc**: Click nút "Phát nhạc" ở góc dưới trái
2. **Điều chỉnh âm lượng**: Kéo thanh trượt Volume
3. **Trạng thái**: Icon thay đổi theo volume (🔇🔉🔊)
4. **Tự động lưu**: Settings được lưu vào localStorage

### Phím tắt
- **H**: Ẩn/hiện các nút điều khiển (bao gồm music controls)

## 🖥️ Yêu cầu hệ thống

### Trình duyệt
- ✅ Chrome 90+ (khuyến nghị)
- ✅ Edge 90+
- ✅ Firefox 88+
- ⚠️ Safari 15+ (có thể không ổn định)

### Phần cứng
- **WebGL 2.0** support
- **Webcam** (cho gesture control)
- **RAM**: Tối thiểu 4GB
- **GPU**: Khuyến nghị có GPU rời cho hiệu suất tốt

## 🎨 Công nghệ sử dụng

- **[Three.js](https://threejs.org/)** v0.160.0 - 3D rendering engine
- **[MediaPipe Hand Landmarker](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker)** - Hand gesture recognition
- **Post-processing**: UnrealBloomPass, Tone Mapping
- **Lighting**: Point lights, Spot lights, Directional lights
- **Materials**: PBR (Physically Based Rendering)

## 📐 Kiến trúc kỹ thuật

### Particle System
- **1500 ornaments**: Vàng, xanh lá, đỏ, candy cane
- **2500 dust particles**: Hiệu ứng tuyết rơi
- **Dynamic positioning**: 3 thuật toán khác nhau cho 3 modes
- **Smooth transitions**: Lerp-based animation giữa các modes

## 📄 License

Code được share tự do cho mục đích học tập và phi thương mại. Vui lòng giữ credit khi sử dụng.

## 🎄 Happy Holidays!

Enjoy your interactive Christmas tree! Merry Christmas and Happy New Year! 🎅✨

---

**Made with ❤️ and Three.js**

*For questions or suggestions, please open an issue.*
