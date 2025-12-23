# 🎄 Interactive Christmas Tree

Cây thông Noel 3D tương tác với điều khiển bằng cử chỉ tay, sử dụng Three.js và MediaPipe Hand Tracking.

## ✨ Tính năng

- **🎨 Particle System 3D**: 4000+ particles với hiệu ứng bloom và lighting chuyên nghiệp
- **👋 Hand Gesture Control**: Điều khiển bằng cử chỉ tay qua webcam
- **📷 Photo Upload**: Thêm ảnh của bạn vào cây thông 3D
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

### Phím tắt
- **H**: Ẩn/hiện các nút điều khiển

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

### Gesture Recognition
```
Pinch Distance < 0.05    → FOCUS Mode
Hand Closed < 0.25       → TREE Mode
Hand Open > 0.4          → SCATTER Mode
```

### Performance
- **Rendering**: WebGL with hardware acceleration
- **Frame rate**: Target 60 FPS
- **Particle count**: Tối ưu cho desktop (có thể giảm trên mobile)
- **Texture**: Procedural candy cane pattern

## 🔧 Cấu hình nâng cao

Chỉnh sửa trong code `noel_v2.html`:

```javascript
const CONFIG = {
    particles: {
        count: 1500,        // Số lượng ornaments
        dustCount: 2500,    // Số lượng dust particles
        treeHeight: 24,     // Chiều cao cây
        treeRadius: 8       // Bán kính cây
    },
    camera: {
        z: 50              // Khoảng cách camera
    }
};
```

## 🐛 Troubleshooting

### Camera không hoạt động
- Kiểm tra quyền truy cập camera trong browser settings
- Thử reload trang và cho phép lại
- Kiểm tra camera có đang được dùng bởi app khác không

### FPS thấp / Lag
- Giảm `CONFIG.particles.count` xuống 500-800
- Giảm `CONFIG.particles.dustCount` xuống 1000
- Tắt các tab/app khác đang chạy
- Thử trình duyệt khác hoặc cập nhật driver GPU

### Gesture không nhận diện
- Đảm bảo đủ ánh sáng
- Đưa tay vào giữa khung hình
- Tránh background phức tạp
- Thử gesture rõ ràng hơn

### Ảnh không upload được
- Kiểm tra định dạng ảnh (JPG, PNG, GIF, WebP)
- Kích thước ảnh nên < 5MB
- Thử upload từng ảnh một

## 📝 Known Issues

- [ ] Chưa có fallback controls khi không có camera
- [ ] Chưa tối ưu cho mobile/touch
- [ ] Memory leak khi upload quá nhiều ảnh (>50)
- [ ] Safari có thể lag hơn Chrome

## 🎯 Roadmap

- [ ] Thêm keyboard/mouse controls cho non-camera devices
- [ ] Mobile touch support
- [ ] Theme switcher (classic, blue, purple)
- [ ] Background music toggle
- [ ] Save/share screenshot feature
- [ ] Performance mode cho low-end devices

## 👏 Credits

- **Original Code**: Tìm được và fix lại bởi [anhduc.onlien](https://anhduc.onlien)
- **Three.js**: [mrdoob](https://github.com/mrdoob) và contributors
- **MediaPipe**: Google MediaPipe team
- **Font**: [Cinzel](https://fonts.google.com/specimen/Cinzel) by Natanael Gama

## 📄 License

Code được share tự do cho mục đích học tập và phi thương mại. Vui lòng giữ credit khi sử dụng.

## 🎄 Happy Holidays!

Enjoy your interactive Christmas tree! Merry Christmas and Happy New Year! 🎅✨

---

**Made with ❤️ and Three.js**

*For questions or suggestions, please open an issue.*
