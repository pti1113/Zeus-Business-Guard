import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { useState } from "react";

export default function ZeusBusinessGuard() {
  const [form, setForm] = useState({ name: "", email: "", message: "" });

  const portfolioItems = [
    {
      title: "국내 각종 전시장 보안전문",
      description:
        "국제 박람회 전시장에서 철저한 출입 통제 및 인물 보호 수행",
    },
    {
      title: "VIP 인물 경호 서비스",
      description: "정치인 및 유명 인사에 대한 일대일 밀착 경호 제공",
    },
    {
      title: "대형 콘서트 행사 경호",
      description: "수천 명이 참여한 콘서트에서 질서 유지 및 무대 주변 보안 담당",
    },
    {
      title: "전문 야외 각종행사 안전관리",
      description: "야외 행사에서의 안전 통제, 인파 관리, 출입 시스템 운영",
    },
    {
      title: "각종 행사 스태프 업무지원",
      description: "행사 진행 보조, 출입 체크 및 안내 요원 운영 등 전반적인 현장 지원",
    },
  ];

  const services = [
    "행사 경호",
    "인물 보호",
    "시설 보안",
    "전시장 보안",
    "경호 아카데미"
  ];

  return (
    <div className="min-h-screen bg-black text-white font-sans">
      {/* Header */}
      <header className="bg-gray-900 p-6 shadow-lg">
        <h1 className="text-3xl font-bold">(주)제우스비즈니스가드</h1>
        <p className="text-gray-400">누구보다 안전하게, 누구보다 전문가답게</p>
      </header>

      {/* Hero Section */}
      <section className="p-10 text-center bg-gray-800">
        <img
          src="https://images.unsplash.com/photo-1603052875812-194f99f8d6aa"
          alt="Main Visual"
          className="w-full max-h-96 object-cover rounded-xl mb-6"
        />
        <h2 className="text-4xl font-bold mb-4">믿음직한 경호, 강력한 보안</h2>
        <p className="text-gray-300 max-w-xl mx-auto">
          행사 경호, 인물 보호, 시설 보안, 전시장 보안까지 —
          제우스비즈니스가드가 책임집니다.
        </p>
      </section>

      {/* 회사 소개 및 연혁 */}
      <section className="p-10 bg-gray-950">
        <h3 className="text-2xl font-bold mb-4">회사 소개</h3>
        <p className="text-gray-300 mb-4">
          (주)제우스비즈니스가드는 킨텍스를 중심으로 활동하며, 고객의 안전을 최우선으로 생각합니다. 축적된 경험과 전문 인력을 바탕으로 각종 행사, 인물, 시설, 전시장에 이르기까지 다양한 보안 서비스를 제공합니다. 믿음직하고 세련된 경호 서비스를 통해 고객의 신뢰를 받고 있습니다.
        </p>
        <h4 className="text-xl font-semibold mt-6 mb-2">회사 연혁</h4>
        <ul className="text-gray-400 list-disc list-inside">
          <li>2018년: 제우스비즈니스가드 설립</li>
          <li>2019년: 국내 대형 박람회 및 행사 보안 서비스 시작</li>
          <li>2021년: VIP 인물 경호 서비스 확대</li>
          <li>2023년: 전시장 야간 순찰 보안 정식 런칭</li>
        </ul>
      </section>

      {/* 조직도 */}
      <section className="p-10 bg-gray-900">
        <h3 className="text-2xl font-bold mb-4">조직도</h3>
        <img
          src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png"
          alt="조직도"
          className="w-full max-w-md mx-auto"
        />
        <p className="text-center text-gray-400 mt-4">
          대표이사 → 운영팀장 → 경호실장 → 팀장/팀원
        </p>
      </section>

      {/* 주요 서비스 */}
      <section className="p-10 bg-gray-800">
        <h3 className="text-2xl font-bold mb-6">주요 서비스</h3>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          {services.map((service) => (
            <Card key={service} className="bg-gray-700 text-white">
              <CardContent className="p-6">
                <h4 className="text-xl font-semibold">{service}</h4>
                <p className="text-gray-400 mt-2">
                  전문 경호 요원이 현장에서 철저히 관리하여 완벽한 안전을 보장합니다.
                </p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* 포트폴리오 */}
      <section className="p-10 bg-gray-950">
        <h3 className="text-2xl font-bold mb-6">포트폴리오</h3>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          {portfolioItems.map((item, index) => (
            <Card key={index} className="bg-gray-800 text-white">
              <CardContent className="p-6">
                <h4 className="text-xl font-semibold">{item.title}</h4>
                <p className="text-gray-400 mt-2">{item.description}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* 문의 폼 */}
      <section className="p-10 bg-gray-950">
        <h3 className="text-2xl font-bold mb-6">문의하기</h3>
        <form className="max-w-xl mx-auto space-y-4">
          <Input
            placeholder="이름"
            value={form.name}
            onChange={(e) => setForm({ ...form, name: e.target.value })}
          />
          <Input
            type="email"
            placeholder="이메일"
            value={form.email}
            onChange={(e) => setForm({ ...form, email: e.target.value })}
          />
          <Textarea
            placeholder="문의 내용을 입력하세요"
            value={form.message}
            onChange={(e) => setForm({ ...form, message: e.target.value })}
          />
          <Button type="submit">보내기</Button>
        </form>
      </section>

      {/* 연락처 */}
      <section className="p-10 bg-gray-900">
        <h3 className="text-2xl font-bold mb-4">연락처</h3>
        <p className="text-gray-300">📞 010-7771-0124</p>
        <p className="text-gray-300">📍 킨텍스</p>
      </section>

      {/* Footer */}
      <footer className="bg-gray-800 text-center p-6 text-gray-400">
        &copy; {new Date().getFullYear()} (주)제우스비즈니스가드. All rights reserved.
      </footer>
    </div>
  );
}
