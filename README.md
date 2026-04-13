# My-Family App — Research & Brainstorm

## 1. Vision

**My-Family** là ứng dụng miễn phí, open-source giúp gia đình Việt:
- Quản lý tài chính chung
- Chia sẻ lịch âm dương
- Kết nối thành viên gia đình

**Tagline:** "Gia đình Việt, một chỗ"

---

## 2. Target Users

| Persona | Mô tả | Pain point |
|---------|--------|------------|
| Mẹ bỉm sữa | Quản lý chi tiêu gia đình, theo dõi lịch tiêm chủng, ngày giỗ | Ghi chép rải rác, hay quên ngày âm |
| Người chồng | Theo dõi thu chi, lên kế hoạch tiết kiệm | Không biết vợ tiêu bao nhiêu |
| Con cái (Gen Z) | Xem lịch gia đình, biết ngày giỗ/đám giỗ | Không nhớ ngày âm |
| Ông bà | Xem lịch âm, ngày lễ, ngày tốt/xấu | Cần app đơn giản, dễ dùng |

---

## 3. Core Features (MVP Phase 1)

### 3.1 Lịch Âm Dương Shared

#### Brainstorm ý tưởng:
- ✅ Xem lịch âm - dương song song
- ✅ Ngày tốt/xấu (hoàng đạo/hắc đạo)
- ✅ Giờ tốt trong ngày
- ✅ Push notification mùng 1, rằm, ngày giỗ
- ✅ Tạo sự kiện trên ngày âm (tự convert sang dương)
- ✅ Share lịch cho thành viên gia đình
- ✅ Countdown Tết âm lịch
- ✅ Widget homescreen (Android/iOS)
- ✅ Danh sách ngày giỗ / thọ / kỵ tự động nhắc
- ✅ Lễ hội truyền thống (Tết Nguyên Đán, Trung Thu, Vu Lan...)
- ✅ Gợi ý "hôm nay nên/không nên làm gì" (phong thủy nhẹ)
- ✅ Nhắc nhở tưới cây/thờ cúng theo ngày

#### Chi tiết:
- Calendar view: tháng, tuần, ngày
- Mặc định hiển thị âm+dương trên mỗi ô
- Sự kiện gia đình hiển thị trên lịch (giỗ, sinh nhật âm, kỷ niệm)
- Member có thể add/edit sự kiện → sync cho cả nhà
- Notification tùy chọn: mùng 1, rằm, giỗ, sinh nhật, lễ tết

### 3.2 Quản Lý Tài Chính Gia Đình

#### Brainstorm ý tưởng:
- ✅ Sổ chi tiêu chung (gia đình)
- ✅ Phân loại: ăn uống, con cái, nhà cửa, xe cộ, y tế, giải trí...
- ✅ Thu nhập & chi tiêu hàng tháng
- ✅ Budget theo danh mục (ví dụ: ăn uống max 5tr/tháng)
- ✅ Số dư chung / ví chung
- ✅ Goal tiết kiệm (mua nhà, du lịch, quỹ hưu trí)
- ✅ Biểu đồ chi tiêu (pie chart, bar chart)
- ✅ Export báo cáo (PDF/Excel)
- ✅ Nhắc nhở trả góp, hóa đơn điện nước
- ✅ Split bill giữa các thành viên
- ✅ Quản lý nợ (cho vay / đi vay)
- ✅ Nhập nhanh bằng giọng nói hoặc OCR hóa đơn
- ✅ Multi-wallet (tiền mặt, thẻ, Momo, ZaloPay)

#### Chi tiết:
- Mỗi giao dịch: số tiền, danh mục, ngày, ghi chú, người chi
- Dashboard tổng quan: thu tháng, chi tháng, số dư, % budget đã dùng
- Biểu đồ xu hướng 6 tháng
- Phê duyệt chi lớn (ví dụ > 500k cần xác nhận từ vợ/chồng) — optional

### 3.3 Gia Đình (Family Hub)

#### Brainstorm ý tưởng:
- ✅ Tạo gia đình → invite thành viên qua link/QR
- ✅ Phân role: Admin (chủ gia đình), Member
- ✅ Profile thành viên (avatar, tên, ngày sinh âm/dương)
- ✅ Khung hình gia đình (family tree đơn giản)
- ✅ Board ghi chú chung (shopping list, to-do)
- ✅ Gallery ảnh chung
- ✅ Location sharing (tùy chọn) — biết con đến trường chưa
- ✅ Nhắc nhở tiêm chủng cho bé
- ✅ Theo dõi chiều cao/cân nặng của con

---

## 4. MVP Scope (Phase 1)

### Làm trước:
1. **Lịch âm shared** — đây là hook chính, ít cạnh tranh
2. **Sổ chi tiêu cơ bản** — thu/chi, danh mục, biểu đồ
3. **Tạo gia đình & invite** — nền tảng cho mọi feature

### Làm sau (Phase 2+):
- Goal tiết kiệm
- Multi-wallet
- OCR hóa đơn
- Family tree
- Location sharing
- Gallery

---

## 5. Tech Stack Đề Xuất

| Layer | Technology | Lý do |
|-------|-----------|-------|
| Frontend | **React Native (Expo)** | Cross-platform, free, community lớn |
| Backend | **Supabase** | Free tier mạnh, auth + realtime + DB |
| Database | **PostgreSQL** (qua Supabase) | Reliable, free |
| Calendar Engine | **lunar-javascript** library | Convert âm dương chính xác |
| Charts | **Victory Native** hoặc **React Native Chart Kit** | Free, đẹp |
| Push Notifications | **Expo Push** | Free, dễ setup |
| Hosting | **Supabase free tier** hoặc **Railway** | Free |
| CI/CD | **GitHub Actions** | Free cho public repo |
| Analytics | **PostHog** (free tier) | Privacy-friendly |

### Tại sao không chọn:
- Flutter → OK nhưng Expo nhanh hơn cho MVP
- Firebase → Google lock-in, Supabase open-source hơn

---

## 6. UI Mockup

Xem file `mockup.html` — mở bằng browser để xem mockup tương tác.

---

## 7. Competitor Analysis

| App | Tính năng | Thiếu | Rating |
|-----|----------|-------|--------|
| **VietCalendar** | Lịch âm, ngày tốt/xấu | Không share, không tài chính | 4.5 |
| **Lịch VN** | Lịch âm, widget | Không collaborative | 4.3 |
| **Honeydue** | Tài chính gia đình | Không có lịch âm, không focus VN | 4.2 |
| **Spendee** | Shared wallet | Không lịch, phí cao | 4.1 |
| **Money Lover** | Chi tiêu VN | Không share gia đình, không lịch âm | 4.5 |
| **Google Calendar** | Shared calendar | Không lịch âm, không tài chính | 4.4 |

**Khoảng trống:** Không ai làm cả lịch âm shared + tài chính gia đình.

---

## 8. Monetization (Giữ free)

- Open source → nhận donation (Buy Me a Coffee, Momo)
- Affiliate nhẹ (sản phẩm tài chính, bảo hiểm) — optional, sau này
- Sponsor từ cộng đồng

---

## 9. Roadmap

### Phase 1 — MVP (8-12 tuần)
- [ ] Setup project (Expo + Supabase)
- [ ] Auth (email, Google, Apple)
- [ ] Family creation & invite
- [ ] Lịch âm dương view
- [ ] Thêm sự kiện trên lịch âm
- [ ] Push notification (mùng 1, rằm, giỗ)
- [ ] Sổ chi tiêu cơ bản
- [ ] Biểu đồ chi tiêu
- [ ] Dashboard gia đình

### Phase 2 — Growth (4-6 tuần)
- [ ] Widget homescreen
- [ ] Goal tiết kiệm
- [ ] Multi-wallet
- [ ] Budget theo danh mục
- [ ] Countdown Tết

### Phase 3 — Scale
- [ ] OCR hóa đơn
- [ ] Voice input
- [ ] Family tree
- [ ] Location sharing
- [ ] Gallery
- [ ] Apple Watch / WearOS

---

## 10. Cấu trúc Folder (Gợi ý)

```
my-family/
├── app/                    # Expo Router screens
│   ├── (auth)/            # Login, Register
│   ├── (tabs)/            # Bottom tabs
│   │   ├── calendar/      # Lịch âm
│   │   ├── finance/       # Tài chính
│   │   ├── family/        # Gia đình
│   │   └── settings/      # Cài đặt
│   └── _layout.tsx
├── components/            # Reusable UI
├── lib/                   # Supabase, utils
├── hooks/                 # Custom hooks
├── assets/                # Images, fonts
├── constants/             # Colors, themes
└── supabase/
    ├── migrations/        # DB schema
    └── seed.sql           # Sample data
```

---

*Tài liệu này sẽ cập nhật khi phát triển.*
