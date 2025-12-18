import React, { useState, useEffect, useMemo } from 'react';
import { BookOpen, Search, ChevronRight, ChevronDown,  Star,  AlertCircle,  CheckCircle, Menu, X, Brain, PenTool, ClipboardCheck } from 'lucide-react';

const ProsthoStudyHub = () => {
  const [activeChapter, setActiveChapter] = useState('ch19');
  const [activeSection, setActiveSection] = useState('intro');
  const [isSidebarOpen, setIsSidebarOpen] = useState(true);
  const [searchQuery, setSearchQuery] = useState('');

  // Data Structure: Contains all content from the provided PDF chapters
  // Wrapped in useMemo to prevent unnecessary re-creations on every render
  const contentData = useMemo(() => ({
    ch19: {
      title: "Chapter 19: 총의치와 발음 (Speech Considerations)",
      icon: <Brain className="w-6 h-6" />,
      sections: {
        intro: {
          title: "1. 발음의 기초와 신경생리",
          content: [
            {
              type: "concept",
              heading: "발음 생성의 개요",
              text: "발음은 신경, 근육, 기계적, 공기역학적 요소가 복합된 무의식적 활동입니다. 구강 구조의 변화는 필연적으로 발음 왜곡을 초래하며, 보철 치료 후 가장 흔한 문제는 발음의 '왜곡(Distortion)'입니다."
            },
            {
              type: "deep-dive",
              heading: "신경생리학적 배경 (Neurophysiological Background)",
              details: [
                "발음은 초당 12~16개의 소리를 내는 빠른 과정입니다.",
                "자동화된 발음 조절: 운동 피질(Premotor and motor cortex)에 국한되며 '최소 노력(Least effort)' 이론이 적용됩니다.",
                "피드백 시스템: 청각(Auditory) 및 구강 감각(Orosensory) 피드백이 중요합니다. 고령 환자는 청력 저하로 적응이 늦어질 수 있습니다.",
                "적응(Adaptation): 초기에는 피드백을 통해 의식적으로 조절하지만, 점차 새로운 운동 프로그램(Engram)이 형성되어 무의식적으로 적응합니다. 보통 2~4주가 소요됩니다."
              ]
            }
          ]
        },
        production: {
          title: "2. 발음 생성과 구강 구조",
          content: [
            {
              type: "concept",
              heading: "자음의 분류와 치아 위치",
              text: "자음은 공기의 흐름이 방해받으며 생성되므로 치아와 의치상의 위치에 민감합니다."
            },
            {
              type: "table",
              heading: "주요 자음과 보철적 고려사항",
              rows: [
                { sound: "양순음 (Bilabial: b, p, m)", organ: "두 입술", check: "입술지지, 수직고경(VDO), 전치부 전후방 위치. 입술 지지가 부족하면 소리가 명확하지 않음." },
                { sound: "순치음 (Labiodental: f, v)", organ: "상악 전치 + 하순", check: "상악 전치 절단연이 하순의 'Wet-dry line'에 닿아야 함. 너무 길면 v가 f처럼, 너무 짧으면 f가 v처럼 들림." },
                { sound: "치설음 (Linguodental: th)", organ: "혀 끝 + 상악 전치", check: "혀가 3~6mm 정도 나와야 함. 3mm 미만이면 치아가 너무 전방, 6mm 이상이면 너무 후방 위치." },
                { sound: "치조설음 (Linguoalveolar: t, d, s, z)", organ: "혀 끝 + 치조제", check: "가장 중요한 's' 발음. 상하악 전치가 닿지 않고 근접해야 함(Closest speaking space: 1~1.5mm)." }
              ]
            },
            {
              type: "clinical",
              heading: "'s' 발음의 중요성 (The 's' Sound)",
              text: "s 발음은 의치 성공 여부의 척도입니다. 혀 끝은 상악 전치 뒤 치조제(Rugae area)에 위치하며, 혀 중앙에 좁은 홈(Groove, 단면적 10mm²)을 형성합니다.",
              tips: [
                "Whistling(휘파람 소리): 구개부 형태가 너무 좁거나 혀의 홈이 좁을 때.",
                "Lisping(sh 소리, 혀짤배기): 공기 통로가 너무 넓거나 혀가 납작해졌을 때.",
                "수직고경 확인: 's' 발음 시 치아 사이가 1~1.5mm 떠야 함 (Closest speaking space)."
              ]
            }
          ]
        },
        troubleshooting: {
          title: "3. 문제 해결 및 프로토콜",
          content: [
            {
              type: "list",
              heading: "발음 문제 해결 프로토콜",
              items: [
                "구의치(Old denture) 확인: 구의치의 구개부 형태와 치아 위치를 복제하면 적응이 빠름.",
                "청력 검사: 청력 손실은 적응을 지연시킴.",
                "치과의사의 모방: 환자의 왜곡된 소리를 의사가 따라해보며 어느 구조물이 방해하는지 파악.",
                "2~4주 대기: 대부분 일시적이므로 즉시 수정하지 않고 적응 기간을 둠."
              ]
            }
          ]
        }
      }
    },
    ch20: {
      title: "Chapter 20: 납의치 형성부터 장착 및 관리",
      icon: <PenTool className="w-6 h-6" />,
      sections: {
        waxing: {
          title: "1. 납의치 형성 (Waxing)",
          content: [
            {
              type: "concept",
              heading: "연마면(Polished Surface)의 중요성",
              text: "의치의 안정성(Stability)과 유지(Retention)는 연마면의 형태에 크게 의존합니다. 근육의 힘이 의치를 안착시키는 방향으로 작용하도록 형성해야 합니다."
            },
            {
              type: "deep-dive",
              heading: "부위별 형성 방법",
              details: [
                "상악 구개부: 두께는 균일하게 2.5mm 유지. 발음을 위해 소구치/견치 부위 구개면은 오목하게(concave) 형성하여 혀 공간 확보.",
                "하악 협측: 제1소구치 부위는 구각결절(Modiolus)의 간섭을 피하기 위해 수직적이거나 오목해야 함.",
                "하악 설측: 혀 공간 확보를 위해 오목(Concave)해야 하지만, 치아 밑으로 너무 깊게 파이면 안 됨(음식물 저류 방지).",
                "치은 형성: 칼날을 45도 각도로 하여 치은 변연 형성. 상악 견치 치근이 가장 길고, 측절치가 가장 짧게 표현."
              ]
            }
          ]
        },
        processing: {
          title: "2. 매몰 및 중합 (Processing)",
          content: [
            {
              type: "list",
              heading: "매몰(Flasking) 과정",
              items: [
                "1단계(Drag): 모형을 하함에 위치. 랜드(Land) 부위는 함의 테두리와 같은 높이로 맞춤.",
                "2단계(Cope): 치아의 절단연과 교두정만 노출시키고 석고를 채움 (선택적).",
                "3단계(Cap): 경석고로 나머지 부분을 채움.",
                "왁스 제거(Boil-out): 끓는 물에 4~6분간 담가 왁스를 연화시킨 후 분리."
              ]
            },
            {
              type: "alert",
              heading: "레진 전입 및 중합 주의사항",
              text: "레진 분리제(Tinfoil substitute)는 치아에 묻지 않도록 주의해야 합니다(결합 실패 원인). 중합은 165°F (73.5°C)에서 9시간 동안 시행하는 것이 일반적이며, 급격한 가열은 기포 발생 및 변형을 초래합니다."
            }
          ]
        },
        insertion: {
          title: "3. 의치 장착 (Insertion)",
          content: [
            {
              type: "clinical",
              heading: "장착 전 준비",
              text: "환자는 내원 12~24시간 전부터 구의치(Old denture)를 착용하지 않아 연조직의 왜곡을 없애야 합니다. 불가능할 경우 Tissue conditioner로 이장하여 조직을 회복시킵니다."
            },
            {
              type: "concept",
              heading: "조정 순서 (Adjustment Sequence)",
              text: "1. 내면 조정 (Basal surface) -> 2. 교합 조정 (Occlusion) -> 3. 연마면 조정 (Polished surface)"
            },
            {
              type: "deep-dive",
              heading: "내면 조정 (PIP 사용법)",
              details: [
                "Pressure Indicator Paste (PIP)를 붓자국이 남도록 얇게 도포.",
                "압박 부위(Pressure spot)는 붓자국이 사라지고 의치상이 드러남. 해당 부위 삭제.",
                "변연 과연장 확인: 변연부에 두껍게 바르고 기능 운동 시킴."
              ]
            },
            {
              type: "concept",
              heading: "교합 조정 (Remounting)",
              text: "구강 내 조정은 연조직의 탄성 때문에 부정확합니다. 반드시 재부착(Remounting)하여 교합기 상에서 조정해야 합니다.",
              subtext: "교합기 재부착을 위해 중심위(CR) 기록을 채득합니다. Aluwax 등을 이용해 치아 접촉 직전까지 닫게 하여 기록."
            },
            {
              type: "list",
              heading: "선택 삭제 (Selective Grinding) 원칙",
              items: [
                "중심위(CR): 교두(Cusp)를 갈지 않고 와(Fossa)를 깊게 파는 것이 원칙 (단, 조기 접촉이 교두 경사면에 있으면 경사면 삭제).",
                "작업측(Working side): 상악 협측 교두의 설측 경사(BULL: Buccal of Upper, Lingual of Lower) 삭제.",
                "균형측(Balancing side): 하악 협측 교두의 설측 경사 삭제 (중심 교두 보호)."
              ]
            }
          ]
        },
        followup: {
          title: "4. 환자 관리 및 검사 (Follow-up)",
          content: [
            {
              type: "clinical",
              heading: "24시간 후 검사 (필수)",
              text: "가장 중요한 검사 시기입니다. 궤양(Sore spot)과 교합 오차를 확인합니다.",
              tips: [
                "Hamular notch 통증: 의치상이 너무 길거나 후방구개폐쇄(PPS)가 너무 강함.",
                "교합 변화: 레진의 수분 흡수로 인해 미세한 교합 변화 발생 가능. 주로 하악 견치/소구치 부위 설측 통증 유발.",
                "구역질(Gagging): 상악 의치 후방 경계가 너무 두껍거나, 진동선(Vibrating line)보다 2mm 이상 연장되었을 때, 혹은 교합 부조화."
              ]
            },
            {
              type: "list",
              heading: "환자 교육 사항",
              items: [
                "저작: 초기에는 무른 음식, 양쪽으로 동시에 씹기.",
                "발음: 소리 내어 책 읽기 연습.",
                "취침: 조직 휴식을 위해 의치를 빼고 물에 담가 보관 (Bone resorption 방지)."
              ]
            }
          ]
        }
      }
    }
  }), []);

  // Filter content based on search query
  const filteredSections = useMemo(() => {
    if (!searchQuery) return null;
    const results = [];
    Object.keys(contentData).forEach(chKey => {
      const chapter = contentData[chKey];
      Object.keys(chapter.sections).forEach(secKey => {
        const section = chapter.sections[secKey];
        // Simple search in title and content text
        const contentStr = JSON.stringify(section.content).toLowerCase();
        if (section.title.toLowerCase().includes(searchQuery.toLowerCase()) || contentStr.includes(searchQuery.toLowerCase())) {
          results.push({ chKey, secKey, title: section.title, chapterTitle: chapter.title });
        }
      });
    });
    return results;
  }, [searchQuery, contentData]);


  const renderContentItem = (item, index) => {
    switch (item.type) {
      case 'concept':
        return (
          <div key={index} className="mb-6 bg-white p-6 rounded-xl shadow-sm border border-gray-100">
            <h3 className="text-lg font-bold text-blue-800 mb-2 flex items-center">
              <BookOpen className="w-5 h-5 mr-2" />
              {item.heading}
            </h3>
            <p className="text-gray-700 leading-relaxed">{item.text}</p>
            {item.subtext && <p className="mt-2 text-sm text-gray-500 italic">{item.subtext}</p>}
          </div>
        );
      case 'deep-dive':
        return (
          <div key={index} className="mb-6 bg-indigo-50 p-6 rounded-xl border-l-4 border-indigo-500">
            <h3 className="text-lg font-bold text-indigo-900 mb-3 flex items-center">
              <Search className="w-5 h-5 mr-2" />
              심화 학습: {item.heading}
            </h3>
            <ul className="space-y-2">
              {item.details.map((detail, idx) => (
                <li key={idx} className="flex items-start text-indigo-800 text-sm">
                  <span className="mr-2 mt-1">•</span>
                  <span>{detail}</span>
                </li>
              ))}
            </ul>
          </div>
        );
      case 'table':
        return (
          <div key={index} className="mb-6 overflow-hidden rounded-xl border border-gray-200">
             <div className="bg-gray-100 p-3 font-bold text-gray-700 text-center">{item.heading}</div>
             <div className="overflow-x-auto">
              <table className="w-full text-sm text-left text-gray-600">
                <thead className="text-xs text-gray-700 uppercase bg-gray-50">
                  <tr>
                    <th className="px-4 py-3">발음</th>
                    <th className="px-4 py-3">관련 구조</th>
                    <th className="px-4 py-3">체크 포인트 (Key Check)</th>
                  </tr>
                </thead>
                <tbody>
                  {item.rows.map((row, idx) => (
                    <tr key={idx} className="bg-white border-b hover:bg-gray-50">
                      <td className="px-4 py-3 font-medium text-gray-900">{row.sound}</td>
                      <td className="px-4 py-3">{row.organ}</td>
                      <td className="px-4 py-3 text-red-600 font-medium">{row.check}</td>
                    </tr>
                  ))}
                </tbody>
              </table>
             </div>
          </div>
        );
      case 'clinical':
        return (
          <div key={index} className="mb-6 bg-green-50 p-5 rounded-xl border border-green-100">
            <h3 className="text-lg font-bold text-green-800 mb-2 flex items-center">
              <Star className="w-5 h-5 mr-2 fill-green-600 text-green-600" />
              Clinical Tip: {item.heading}
            </h3>
            <p className="text-gray-800 mb-3">{item.text}</p>
            {item.tips && (
              <div className="bg-white p-4 rounded-lg border border-green-100">
                <ul className="space-y-1">
                  {item.tips.map((tip, idx) => (
                    <li key={idx} className="flex items-start text-sm text-gray-600">
                      <CheckCircle className="w-4 h-4 mr-2 mt-0.5 text-green-500 shrink-0" />
                      {tip}
                    </li>
                  ))}
                </ul>
              </div>
            )}
          </div>
        );
      case 'alert':
        return (
          <div key={index} className="mb-6 bg-red-50 p-4 rounded-xl flex items-start border border-red-100">
            <AlertCircle className="w-6 h-6 text-red-500 mr-3 mt-1 shrink-0" />
            <div>
              <h3 className="font-bold text-red-800 mb-1">{item.heading}</h3>
              <p className="text-red-700 text-sm">{item.text}</p>
            </div>
          </div>
        );
      case 'list':
        return (
          <div key={index} className="mb-6 bg-white p-6 rounded-xl shadow-sm border border-gray-100">
             <h3 className="text-lg font-bold text-gray-800 mb-4 flex items-center">
               <ClipboardCheck className="w-5 h-5 mr-2 text-blue-600" />
               {item.heading}
             </h3>
             <ol className="list-decimal pl-5 space-y-2 text-gray-700">
               {item.items.map((it, idx) => (
                 <li key={idx} className="pl-1">{it}</li>
               ))}
             </ol>
          </div>
        );
      default:
        return null;
    }
  };

  // Safe getter for current section
  const currentChapter = contentData[activeChapter];
  const currentSection = currentChapter?.sections[activeSection];

  return (
    <div className="flex h-screen bg-gray-50 font-sans text-gray-900 overflow-hidden">
      {/* Mobile Sidebar Overlay */}
      {!isSidebarOpen && (
        <button 
          onClick={() => setIsSidebarOpen(true)}
          className="fixed top-4 left-4 z-50 p-2 bg-blue-900 text-white rounded-md shadow-lg lg:hidden hover:bg-blue-800 transition-colors"
        >
          <Menu className="w-6 h-6" />
        </button>
      )}

      {/* Sidebar Navigation */}
      <div 
        className={`fixed inset-y-0 left-0 z-40 w-80 bg-slate-900 text-white transform transition-transform duration-300 ease-in-out lg:relative lg:translate-x-0 ${
          isSidebarOpen ? 'translate-x-0' : '-translate-x-full'
        }`}
      >
        <div className="flex flex-col h-full">
          <div className="p-6 border-b border-slate-700 flex justify-between items-center bg-slate-800">
            <div>
              <h1 className="text-xl font-extrabold tracking-tight text-white">총의치 마스터</h1>
              <p className="text-xs text-slate-400 mt-1">Zarb's Prosthodontics Ch 19-20</p>
            </div>
            <button onClick={() => setIsSidebarOpen(false)} className="lg:hidden text-slate-400 hover:text-white">
              <X className="w-6 h-6" />
            </button>
          </div>

          <div className="p-4 border-b border-slate-700 bg-slate-900 sticky top-0">
            <div className="relative">
              <Search className="absolute left-3 top-2.5 w-4 h-4 text-slate-500" />
              <input
                type="text"
                placeholder="검색 (예: hamular notch)"
                className="w-full bg-slate-800 text-sm text-white rounded-lg pl-10 pr-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500 placeholder-slate-500"
                value={searchQuery}
                onChange={(e) => setSearchQuery(e.target.value)}
              />
            </div>
          </div>

          <nav className="flex-1 overflow-y-auto p-4 space-y-6">
            {searchQuery ? (
               // Search Results View
               <div>
                 <h3 className="text-xs font-semibold text-slate-400 uppercase tracking-wider mb-3">검색 결과</h3>
                 {filteredSections && filteredSections.length > 0 ? (
                   <ul className="space-y-2">
                     {filteredSections.map((result, idx) => (
                       <li key={idx}>
                         <button
                           onClick={() => {
                             setActiveChapter(result.chKey);
                             setActiveSection(result.secKey);
                             setSearchQuery('');
                             if(window.innerWidth < 1024) setIsSidebarOpen(false);
                           }}
                           className="w-full text-left p-3 rounded-lg bg-slate-800 hover:bg-slate-700 transition-colors border border-slate-700"
                         >
                           <div className="text-xs text-blue-400 mb-1">{result.chapterTitle}</div>
                           <div className="text-sm font-medium">{result.title}</div>
                         </button>
                       </li>
                     ))}
                   </ul>
                 ) : (
                   <div className="text-sm text-slate-500 text-center py-4">검색 결과가 없습니다.</div>
                 )}
               </div>
            ) : (
              // Standard Navigation View
              Object.keys(contentData).map((chKey) => (
                <div key={chKey}>
                  <button
                    onClick={() => {
                      if (activeChapter !== chKey) {
                        setActiveChapter(chKey);
                        // Reset to the first section of the new chapter to avoid referencing a non-existent section
                        setActiveSection(Object.keys(contentData[chKey].sections)[0]);
                      }
                    }}
                    className={`w-full flex items-center justify-between p-2 rounded-lg transition-colors ${activeChapter === chKey ? 'text-white font-bold' : 'text-slate-400 hover:text-white'}`}
                  >
                    <div className="flex items-center">
                      {contentData[chKey].icon}
                      <span className="ml-3 text-sm">{contentData[chKey].title}</span>
                    </div>
                    {activeChapter === chKey ? <ChevronDown className="w-4 h-4" /> : <ChevronRight className="w-4 h-4" />}
                  </button>
                  
                  {activeChapter === chKey && (
                    <div className="mt-2 ml-4 pl-4 border-l-2 border-slate-700 space-y-1">
                      {Object.keys(contentData[chKey].sections).map((secKey) => (
                        <button
                          key={secKey}
                          onClick={() => {
                            setActiveSection(secKey);
                            if(window.innerWidth < 1024) setIsSidebarOpen(false);
                          }}
                          className={`w-full text-left text-sm py-2 px-3 rounded-md transition-all ${
                            activeSection === secKey 
                              ? 'bg-blue-600 text-white font-medium shadow-lg' 
                              : 'text-slate-400 hover:text-white hover:bg-slate-800'
                          }`}
                        >
                          {contentData[chKey].sections[secKey].title}
                        </button>
                      ))}
                    </div>
                  )}
                </div>
              ))
            )}
          </nav>
          
          <div className="p-4 border-t border-slate-800 text-xs text-center text-slate-500">
            Based on Zarb's Prosthodontic Treatment
          </div>
        </div>
      </div>

      {/* Main Content Area */}
      <main className="flex-1 overflow-y-auto bg-gray-50 relative w-full">
        <div className="max-w-4xl mx-auto p-6 lg:p-10 pb-20">
          {/* Safeguard: Ensure content exists before rendering */}
          {!currentSection ? (
            <div className="flex items-center justify-center h-64 text-gray-500">
              Loading content...
            </div>
          ) : (
            <>
              {/* Header */}
              <header className="mb-8 pb-6 border-b border-gray-200">
                <div className="flex items-center text-sm text-blue-600 font-semibold mb-2 uppercase tracking-wide">
                  <span className="bg-blue-100 px-2 py-1 rounded mr-2">Study Mode</span>
                  {currentChapter.title.split(':')[0]}
                </div>
                <h1 className="text-3xl lg:text-4xl font-extrabold text-gray-900 mb-3">
                  {currentSection.title}
                </h1>
                <p className="text-gray-500 text-lg">
                  {activeChapter === 'ch19' ? '발음의 원리와 보철적 고려사항' : '의치 제작의 마무리와 장착 후 관리'}
                </p>
              </header>

              {/* Dynamic Content */}
              <div className="space-y-4 animate-fadeIn">
                {currentSection.content.map((item, index) => 
                  renderContentItem(item, index)
                )}
              </div>

              {/* Navigation Footer */}
              <div className="mt-12 pt-8 border-t border-gray-200 flex justify-between">
                <button 
                  className="flex items-center text-gray-500 hover:text-blue-600 transition-colors disabled:opacity-30"
                  disabled={Object.keys(currentChapter.sections).indexOf(activeSection) === 0 && activeChapter === 'ch19'}
                  onClick={() => {
                     const sections = Object.keys(currentChapter.sections);
                     const currIdx = sections.indexOf(activeSection);
                     if (currIdx > 0) setActiveSection(sections[currIdx - 1]);
                     else if (activeChapter === 'ch20') {
                       setActiveChapter('ch19');
                       const prevSections = Object.keys(contentData['ch19'].sections);
                       setActiveSection(prevSections[prevSections.length - 1]);
                     }
                  }}
                >
                  <ChevronRight className="w-5 h-5 rotate-180 mr-1" />
                  이전 섹션
                </button>

                <button 
                  className="flex items-center font-medium text-blue-600 hover:text-blue-800 transition-colors disabled:opacity-30"
                  disabled={Object.keys(currentChapter.sections).indexOf(activeSection) === Object.keys(currentChapter.sections).length - 1 && activeChapter === 'ch20'}
                  onClick={() => {
                     const sections = Object.keys(currentChapter.sections);
                     const currIdx = sections.indexOf(activeSection);
                     if (currIdx < sections.length - 1) setActiveSection(sections[currIdx + 1]);
                     else if (activeChapter === 'ch19') {
                       setActiveChapter('ch20');
                       setActiveSection(Object.keys(contentData['ch20'].sections)[0]);
                     }
                  }}
                >
                  다음 섹션
                  <ChevronRight className="w-5 h-5 ml-1" />
                </button>
              </div>
            </>
          )}
        </div>
      </main>
    </div>
  );
};

export default ProsthoStudyHub;
