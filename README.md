<p align="center">
  <img src="./assets/header.svg" alt="Genesis header" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=22&duration=2800&pause=600&color=A78BFA&center=true&vCenter=true&width=900&lines=Software+Engineer;Systems+as+stories%2C+code+as+craft;Outcomes+over+output;TypeScript+%7C+Python+%7C+C%2FC%2B%2B+%7C+Rust+%7C+Elixir" alt="Typing headline" />
</p>

<p align="center">
  <a href="https://github.com/gns-x"><img src="https://img.shields.io/badge/Genesis-AI%20%7C%20LangChain%20%26%20Agents-6EE7F9?style=for-the-badge&logo=github" alt="Profile" /></a>
</p>

## Signal

- Role: Software Engineer
- Languages I think in: TypeScript • Python • C • C++ • Rust • Elixir
- Interests: AI systems, LangChain, agents, RAG, tool-use, orchestration, LLM evals

## Constellation of Craft

```mermaid
%%{init: {'theme': 'dark', 'themeVariables': { 'primaryColor': '#1F2937', 'secondaryColor': '#4C1D95', 'tertiaryColor': '#6EE7F9', 'lineColor': '#A78BFA', 'textColor': '#E5E7EB'}}}%%
mindmap
  root((Genesis))
    Languages
      TypeScript
        React/TSX
        Node
        Tooling
      Python
        Data
        FastAPI
        Automation
      C
        OS
        Perf
      C++
        Concurrency
        Toolchains
      Rust
        Systems
        CLIs
      Elixir
        Phoenix LiveView
        OTP
    Domains
      DX & Tooling
      Distributed Systems
      Real‑time Interfaces
      Compiler Curious
    Values
      Clarity
      Performance
      Reliability
      Ergonomics
```

 

## Signature Kata (one idea, six tongues)

<details>
<summary><b>TypeScript</b> — ergonomic edges</summary>

```ts
export function stabilize<T>(items: T[], key: (x: T) => string): T[] {
  const seen = new Set<string>();
  return items.filter(item => {
    const k = key(item);
    if (seen.has(k)) return false;
    seen.add(k);
    return true;
  });
}
```
</details>

<details>
<summary><b>Python</b> — expressive minimalism</summary>

```python
from typing import Callable, Iterable, TypeVar
T = TypeVar("T")

def stabilize(items: Iterable[T], key: Callable[[T], str]) -> list[T]:
    seen: set[str] = set()
    out: list[T] = []
    for x in items:
        k = key(x)
        if k in seen:
            continue
        seen.add(k)
        out.append(x)
    return out
```
</details>

<details>
<summary><b>C++</b> — zero‑cost abstractions</summary>

```cpp
#include <unordered_set>
#include <vector>
template <typename T, typename F>
std::vector<T> stabilize(const std::vector<T>& items, F key) {
  std::unordered_set<std::string> seen;
  std::vector<T> out;
  out.reserve(items.size());
  for (const auto& x : items) {
    auto k = key(x);
    if (seen.insert(k).second) out.push_back(x);
  }
  return out;
}
```
</details>

<details>
<summary><b>Rust</b> — fearless correctness</summary>

```rust
use std::collections::HashSet;
pub fn stabilize<T, F>(items: impl IntoIterator<Item = T>, mut key: F) -> Vec<T>
where
    F: FnMut(&T) -> String,
{
    let mut seen = HashSet::new();
    let mut out = Vec::new();
    for x in items {
        let k = key(&x);
        if seen.insert(k) {
            out.push(x);
        }
    }
    out
}
```
</details>

<details>
<summary><b>Elixir</b> — concurrent clarity</summary>

```elixir
defmodule Genesis do
  def stabilize(items, key) do
    Enum.reduce(items, {MapSet.new(), []}, fn x, {seen, out} ->
      k = key.(x)
      if MapSet.member?(seen, k), do: {seen, out}, else: {MapSet.put(seen, k), [x | out]}
    end)
    |> elem(1)
    |> Enum.reverse()
  end
end
```
</details>

## Live Signals

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=gns-x&show_icons=true&count_private=true&theme=tokyonight&rank_icon=github" alt="GitHub Stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=gns-x&layout=compact&langs_count=8&theme=tokyonight" alt="Top Languages" />
</p>

---

If you’ve read this far, we should probably build something together.

