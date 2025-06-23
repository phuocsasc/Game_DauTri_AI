<!-- PHẦN 1: SETUP GAME -->
            <section id="setup-game" class="mb-10">
                  <h2 class="text-xl font-semibold mb-4">1. Setup Game</h2>
                  <div class="space-y-4">
                        <div class="flex justify-between items-center">
                              <h3 class="text-lg font-medium">Thông Tin Các Đội Chơi</h3>
                              <div class="space-x-2">
                                    <button onclick="openTeamModal()" class="bg-blue-500 text-white px-3 py-1 rounded">+
                                          Thêm đội</button>
                                    <button onclick="resetTeams()" class="bg-red-600 text-white px-3 py-1 rounded">Reset
                                          Dữ Liệu</button>
                              </div>
                        </div>
                        <div id="teams-container" class="grid grid-cols-1 md:grid-cols-2 gap-4"></div>
                  </div>
            </section>


// Thành nào có appearsAtRound <= round thì sẽ hiển thị (tồn tại liên tục từ đó đến vòng 7)
                  const currentCastles = castles.filter(c => {
                        const appearRound = parseInt(c.appearsAtRound) || 1; // Nếu không có, mặc định là vòng 1
                        return appearRound <= round;
                  });